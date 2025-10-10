# Processes and Jobs

## Resuming Processes
To resume processes, your shell provides the fg command, a builtin that takes the suspended process,
### Solve
**Flag:** `pwn.college{w3jmzyeFf8h8Czi0WYbdkkxdakr.QX2QDO0wiN5AzNzEzW}`

Running the command to force quit and then resuming it by using fg. 

```bash
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ jobs
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg %1
/challenge/run
I'm back! Here's your flag:
pwn.college{w3jmzyeFf8h8Czi0WYbdkkxdakr.QX2QDO0wiN5AzNzEzW}
Don't forget to press Enter to quit me!

Goodbye!
```

### New Learnings
Using of fg command.

### References 
Add any references or videos you used while solving the challenge.
