# Processes and Jobs

## Suspending Processes 
You can suspend processes to the background with Ctrl-Z.

### Solve
**Flag:** `pwn.college{cLeJjVvBpu3pIOqcuM1XznFuocV.QX1QDO0wiN5AzNzEzW}`

Running the command directly /callenge/run then ctrl+z forcing to copy of it's own.

```bash
/challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         161     142  0 06:48 pts/0    00:00:00 bash /challenge/run
root         163     161  0 06:48 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can
background me with Ctrl-Z or, if you're not ready to do that for whatever
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         161     142  0 06:48 pts/0    00:00:00 bash /challenge/run
root         168     142  0 06:48 pts/0    00:00:00 bash /challenge/run
root         170     168  0 06:48 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{cLeJjVvBpu3pIOqcuM1XznFuocV.QX1QDO0wiN5AzNzEzW}
```

### New Learnings
Using of Ctrl+z to copy. 
### References 
Add any references or videos you used while solving the challenge.
