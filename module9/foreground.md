# Processes and Jobs

## Foregrounding processes
 you can foreground a backgrounded process with fg just like you foreground a suspended process! This level will walk you through that!

### Solve
**Flag:** `pwn.college{0Tx_gKw_Lva1_Y4pARObb93qXhW.QX4QDO0wiN5AzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@processes~foregrounding-processes:~$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the
background, and *then* foreground it without re-suspending it! You can
background me with Ctrl-Z (and resume me in the background with 'bg') or, if
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg %1
[1]+ /challenge/run &
hacker@processes~foregrounding-processes:~$


Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out. After that, resume me into the foreground with 'fg';
I'll wait.

hacker@processes~foregrounding-processes:~$ fg %1
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{0Tx_gKw_Lva1_Y4pARObb93qXhW.QX4QDO0wiN5AzNzEzW}
```

### New Learnings
Forgrounding the background processes.

### References 
Add any references or videos you used while solving the challenge.
