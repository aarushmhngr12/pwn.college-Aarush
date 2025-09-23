# Comprehending Commands

## Grepping for a needle in a haystack
using grep command to search for the flag starting with pwn.college in the /challenge/data.txt which has hundred thousands lines.

### Solve
**Flag:** `pwn.college{k6k2cDum_H6_Ga1oRV1nqO14fGX.QX3EDO0wiN5AzNzEzW}`

Firstly I tried it out with some random word like flag itself. It showed me a list of words containing flag word in it.
then i used the 'pwn.college' which was the hint .

```bash
grep 'pwn.college' /challenge/data.txt
pwn.college{k6k2cDum_H6_Ga1oRV1nqO14fGX.QX3EDO0wiN5AzNzEzW}
```

### New Learnings
Grep command for taking out the content out of the file.

### References 
Add any references or videos you used while solving the challenge.
