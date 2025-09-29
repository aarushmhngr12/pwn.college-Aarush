# Praticing Piping

## Grepping Errors
The shell has a >& operator, which redirects a file descriptor to another file descriptor.
This means that we can have a two-step process to grep through errors: 
first, we redirect standard error to standard output (2>& 1) and then pipe the now-combined stderr and stdout as normal (|)!

### Solve
**Flag:** `pwn.college{QiMjOHGdJcqk___7uIJppOmVkVq.QX1ATO0wiN5AzNzEzW}`

Using the /challenge/run 2>&1 which would send the errors to stdout.
and then using grep pwn to fiter the hundreds of texts to get the flag.

```bash
/challenge/run  2>&1 | grep pwn
[PASS] Success! You have satisfied all execution requirements.
pwns
pwn.college{QiMjOHGdJcqk___7uIJppOmVkVq.QX1ATO0wiN5AzNzEzW}
pwn
pwned
pwning
```

### New Learnings
Using of >& operator to redirect the stderr to stdout.

### References 
Add any references or videos you used while solving the challenge.
