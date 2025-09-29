# Practicing Piping

## Filtering with grep -v
Use grep -v to filter out all the lines containing "DECOY" and reveal the real flag!

### Solve
**Flag:** `pwn.college{4dzrBtHsUchLt2ikOzIzqR0L2jP.0FOxEzNxwiN5AzNzEzW}`

I used the pipe operator between rrunning the challenge and greeping -v command withthe word "DECOY".

```bash
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{4dzrBtHsUchLt2ikOzIzqR0L2jP.0FOxEzNxwiN5AzNzEzW}
```

### New Learnings
Use of grep -v word to filter out the text containing the word.

### References 
Add any references or videos you used while solving the challenge.
