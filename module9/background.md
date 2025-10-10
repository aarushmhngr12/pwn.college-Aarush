# Processes and Jobs

## Background Processes
You've resumed processes in the foreground with the fg command.
You can also resume processes in the background with the bg command!
This will allow the process to keep running, while giving you your shell back to invoke more commands in the meantime.

### Solve
**Flag:** `pwn.college{k2s1t_OVFEHWHONlVEY0UZeRLfI.QX3QDO0wiN5AzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@processes~backgrounding-processes:~$ sleep 1337
^Z
[1]+  Stopped                 sleep 1337
hacker@processes~backgrounding-processes:~$ bg
[1]+ sleep 1337 &
hacker@processes~backgrounding-processes:~$ ps -o user,pid,stat,cmd
USER         PID STAT CMD
hacker       151 Ss   /run/dojo/bin/bash --login
hacker       165 S    sleep 1337
hacker       166 R+   ps -o user,pid,stat,cmd
hacker@processes~backgrounding-processes:~$ ./challenge/run
bash: ./challenge/run: No such file or directory
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         168 S+   bash /challenge/run
root         170 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the 
background, and then launch a new version of me! You can background me with 
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to 
do that for whatever reason, just hit Enter and I'll exit!
^Z
[2]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[2]+ /challenge/run &
hacker@processes~backgrounding-processes:~$ 


Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out.

hacker@processes~backgrounding-processes:~$ ^C
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         168 S    bash /challenge/run
root         178 S    sleep 6h
root         179 S+   bash /challenge/run
root         181 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{k2s1t_OVFEHWHONlVEY0UZeRLfI.QX3QDO0wiN5AzNzEzW}
```

### New Learnings
Using of bg command.

### References 
Add any references or videos you used while solving the challenge.
