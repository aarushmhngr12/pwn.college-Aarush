# Processes and Jobs

## Interrupting Processes
Try it here! /challenge/run will refuse to give you the flag until you interrupt it. Good luck!

For the very interested, check out this article about terminals and "control codes" (such as Ctrl-C).

### Solve
**Flag:** `pwn.college{w6xgHCeEeWyw3-6-6h89qEcGXs3.QXzQDO0wiN5AzNzEzW}`

Directly running the /challenge/run and then forcing to execute it by using ctrl+c.

```bash
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember,
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{w6xgHCeEeWyw3-6-6h89qEcGXs3.QXzQDO0wiN5AzNzEzW}
```

### New Learnings
Using Ctrl+c to force the command to execute.

### References 
Add any references or videos you used while solving the challenge.
