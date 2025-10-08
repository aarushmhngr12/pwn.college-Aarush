## Bratcha
converted all of 286 possiblities in a python code ran it and found the flag
https://pastebin.com/sqxnxBhZ
```bash
#!/usr/bin/env python3
"""
pastebin_enum_descriptive.py

Elaborated version of brute-force URL enumerator with descriptive variable names.
Features:
  - validated character mapping
  - deterministic key ordering
  - progress reporting
  - optional dry-run mode
  - polite rate-limiting
"""

from __future__ import annotations
import argparse
import itertools
import json
import logging
import math
import sys
import time
from typing import Dict, List, Sequence, Tuple, Optional

import requests

# Default mapping of positions to possible characters
DEFAULT_POSITION_CHAR_MAP = {
    '1': ['c','s'],
    '2': ['g','q'],
    '3': ['x','y'],
    '4': ['n','h'],
    '5': ['x','v'],
    '6': ['B','D'],
    '7': ['n','h'],
    '8': ['S','Z']
}

SAFETY_NOTICE = (
    "WARNING: Only run this script against servers/URLs you own or have explicit "
    "permission to test. Automated enumeration may discover private content and "
    "could violate terms of service or law."
)

def validate_position_char_map(position_char_map: Dict[str, Sequence[str]]) -> List[str]:
    """
    Validate the character mapping and return a deterministic list of keys.
    Raises TypeError/ValueError on invalid input.
    """
    if not isinstance(position_char_map, dict):
        raise TypeError("position_char_map must be a dictionary")

    if not position_char_map:
        raise ValueError("position_char_map cannot be empty")

    for position, char_list in position_char_map.items():
        if not isinstance(position, str):
            raise TypeError(f"Position {position!r} must be a string")
        if not isinstance(char_list, (list, tuple)):
            raise TypeError(f"position_char_map[{position!r}] must be a list or tuple")
        if not char_list:
            raise ValueError(f"position_char_map[{position!r}] cannot be empty")
        for character in char_list:
            if not isinstance(character, str) or len(character) != 1:
                raise ValueError(f"Character {character!r} in position {position!r} must be a single string")

    # Sort keys numerically if possible, otherwise lexicographically
    try:
        sorted_keys = sorted(position_char_map.keys(), key=int)
    except ValueError:
        sorted_keys = sorted(position_char_map.keys())

    return sorted_keys

def calculate_total_combinations(position_char_map: Dict[str, Sequence[str]], ordered_positions: List[str]) -> int:
    return math.prod(len(position_char_map[pos]) for pos in ordered_positions)

def generate_urls(base_url: str, position_char_map: Dict[str, Sequence[str]], ordered_positions: List[str]):
    """
    Generator yielding (index, combination_string, full_url) for each combination.
    """
    character_options = [position_char_map[pos] for pos in ordered_positions]
    for index, combo_tuple in enumerate(itertools.product(*character_options), start=1):
        combination_string = ''.join(combo_tuple)
        full_url = base_url.rstrip('/') + '/' + combination_string
        yield index, combination_string, full_url

def fetch_url(session: requests.Session, target_url: str, timeout_seconds: float) -> Tuple[Optional[int], Optional[str]]:
    """
    Make a GET request safely. Returns (status_code, response_text), or (None, None) on failure.
    """
    try:
        response = session.get(target_url, timeout=timeout_seconds, allow_redirects=True)
        return response.status_code, response.text
    except requests.RequestException as error:
        logging.debug("Request failed for %s: %s", target_url, error)
        return None, None

def parse_arguments() -> argparse.Namespace:
    parser = argparse.ArgumentParser(
        description="Enumerate pastebin-like URLs using a position->character mapping."
    )
    parser.add_argument("--base-url", "-b", default="https://pastebin.com/", help="Base URL to enumerate (default: https://pastebin.com/)")
    parser.add_argument("--mapping-file", "-m", help="JSON file with position-character mapping (overrides default).")
    parser.add_argument("--request-delay", type=float, default=0.5, help="Delay between requests in seconds (default: 0.5)")
    parser.add_argument("--timeout", type=float, default=6.0, help="Request timeout in seconds (default: 6.0)")
    parser.add_argument("--report-every", type=int, default=100, help="Report progress every N attempts (default: 100)")
    parser.add_argument("--stop-on-first", action="store_true", help="Stop after first matching URL is found")
    parser.add_argument("--dry-run", action="store_true", help="Generate URLs without making HTTP requests")
    parser.add_argument("--dry-run-count", type=int, default=20, help="Number of URLs to generate in dry-run mode")
    parser.add_argument("--save-file", default="found_urls.txt", help="File to save found URLs")
    parser.add_argument("--verbose", "-v", action="store_true", help="Enable DEBUG logging")
    parser.add_argument("--force", action="store_true", help="Force execution even if total combinations are large")
    parser.add_argument("--max-total-warn", type=int, default=200000, help="Warn if total combinations exceed this number")
    return parser.parse_args()

def main():
    args = parse_arguments()

    logging.basicConfig(
        level=logging.DEBUG if args.verbose else logging.INFO,
        format="%(asctime)s [%(levelname)s] %(message)s",
    )

    print(SAFETY_NOTICE)

    # Load mapping
    if args.mapping_file:
        try:
            with open(args.mapping_file, 'r', encoding='utf-8') as file_handle:
                position_char_map = json.load(file_handle)
            if not isinstance(position_char_map, dict):
                logging.error("Mapping file must contain a JSON object (dict).")
                sys.exit(1)
        except Exception as error:
            logging.exception("Failed to load mapping file: %s", error)
            sys.exit(1)
    else:
        position_char_map = DEFAULT_POSITION_CHAR_MAP

    # Validate mapping and order keys
    try:
        ordered_positions = validate_position_char_map(position_char_map)
    except Exception as error:
        logging.exception("Invalid mapping: %s", error)
        sys.exit(1)

    logging.info("Ordered positions: %s", ordered_positions)
    for pos in ordered_positions:
        logging.debug("position_char_map[%s] -> %r", pos, position_char_map[pos])

    total_combos = calculate_total_combinations(position_char_map, ordered_positions)
    logging.info("Total combinations to try: %d", total_combos)
    if total_combos > args.max_total_warn and not args.force:
        logging.error("Total combinations (%d) exceed warning threshold (%d). Use --force to proceed.", total_combos, args.max_total_warn)
        sys.exit(2)

    if args.dry_run:
        logging.info("Dry run: generating first %d URLs", args.dry_run_count)
        for index, combo_string, full_url in itertools.islice(generate_urls(args.base_url, position_char_map, ordered_positions), args.dry_run_count):
            print(f"{index:6d}  {combo_string}  ->  {full_url}")
        return

    session = requests.Session()
    session.headers.update({"User-Agent": "pastebin-enum-descriptive/1.0"})
    found_urls: List[str] = []
    start_time = time.time()

    try:
        for index, combo_string, full_url in generate_urls(args.base_url, position_char_map, ordered_positions):
            status_code, page_content = fetch_url(session, full_url, timeout_seconds=args.timeout)
            if status_code == 200 and page_content and args.base_url.replace("https://", "").replace("http://", "").split('/')[0] in page_content:
                logging.info("[!] Found URL #%d: %s", index, full_url)
                found_urls.append(full_url)
                with open(args.save_file, "a", encoding="utf-8") as save_file:
                    save_file.write(full_url + "\n")
                if args.stop_on_first:
                    break
            else:
                logging.debug("Tried #%d: %s -> status=%s", index, full_url, status_code)

            if index % args.report_every == 0 or index == total_combos:
                elapsed = time.time() - start_time
                pct = (index / total_combos) * 100 if total_combos else 0.0
                logging.info("Progress: %d/%d (%.2f%%) elapsed: %.1fs", index, total_combos, pct, elapsed)

            time.sleep(args.request_delay)

    except KeyboardInterrupt:
        logging.warning("Interrupted by user. Saving progress and exiting.")
    except Exception as error:
        logging.exception("Unexpected error during enumeration: %s", error)

    if found_urls:
        logging.info("Found %d URL(s). Results appended to %s", len(found_urls), args.save_file)
    else:
        logging.info("No matching URLs found.")

if __name__ == "__main__":
    main()
```
