# Data Manipulation

## Sorting Data
there's a file at /challenge/flags.txt containing 100 fake flags,
with the real flag mixed among them. When sorted alphabetically, 
the real flag will be at the end

### Solve
**Flag:** `pwn.college{w7UjtEjWuKBYn3zeWno7FE7sKN6.0FM0MDOxwiN5AzNzEzW}`

What i thought is to use sort -r order as we were told to use to get the flag at the end but i wanted it at the first position.
``` bash
sort -r /challenge/flags.txt
pwn.college{w7UjtEjWuKBYn3zeWno7FE7sKN6.0FM0MDOxwiN5AzNzEzW}
pwn.college{w7UjtEjWuKBYn3zeWno7FE7sKN6.0FM0MDOxwiM5AzNzEzW}
.
.
.
```

### New Learnings
Using of sort and its operator to sort the lines of the text accordingly.

### References 
Add any references or videos you used while solving the challenge.
