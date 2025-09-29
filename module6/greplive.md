# Praticing Piping

## Grepping Live Output
 /challenge/run will output a hundred thousand lines of text, use pipe perator,  including the flag. grep for the flag!

### Solve
**Flag:** `pwn.college{kbu6wmmbLUVhvU_p8CviPDhDMAm.QX5EDO0wiN5AzNzEzW}`

USing the direct command of running the challenge and using pipe command and grep to filter the pwn codes.

```bash
/challenge/run | grep pwn
pwned
pwns
pwn
pwning
pwn.college{kbu6wmmbLUVhvU_p8CviPDhDMAm.QX5EDO0wiN5AzNzEzW}
```

### New Learnings
Using of PIPE operator.

### References 
Add any references or videos you used while solving the challenge.
