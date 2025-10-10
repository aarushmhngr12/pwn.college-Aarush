# Processes and Jobs

## Process Exit Codes
In this challenge, you must retrieve the exit code returned by /challenge/get-code and then run /challenge/submit-code with that error code as an argument. 

### Solve
**Flag:** `pwn.college{04z2F55vs_dFjGMpYN-De5d1BiV.QX5YDO1wiN5AzNzEzW}`

As told to use the exit codes at an instant

```bash
hacker@processes~process-exit-codes:~$  /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ /challenge/submit-code $?
CORRECT! Here is your flag:
pwn.college{04z2F55vs_dFjGMpYN-De5d1BiV.QX5YDO1wiN5AzNzEzW}
```

### New Learnings
Using $?.

### References 
Add any references or videos you used while solving the challenge.
