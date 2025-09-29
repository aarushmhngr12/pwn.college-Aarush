# Praticing Piping

## Grepping Stored Result
In preparation for more complex levels, we want you to:

Redirect the output of /challenge/run to /tmp/data.txt.
This will result in a hundred thousand lines of text, with one of them being the flag, in /tmp/data.txt.
grep that for the flag!

### Solve
**Flag:** `pwn.college{Ubw21JwcJKzXphNzk-1ZyhG-DJk.QX4EDO0wiN5AzNzEzW}`

Redirecting the ouput then using the grep command in the file.

```bash
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
grep pwn /tmp/data.txt
pwn
pwned
pwn.college{Ubw21JwcJKzXphNzk-1ZyhG-DJk.QX4EDO0wiN5AzNzEzW}
pwns
pwning
```

### New Learnings
Using grep command during the rdirecting of outputs.

### References 
Add any references or videos you used while solving the challenge.
