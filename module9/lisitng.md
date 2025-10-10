# Processes and Jobs

## Listing Processes
ps output may truncate long command lines to fit your terminal width, 
hiding full paths.
Enlarge the terminal, redirect output, or use double w 
(e.g., ps -efww or ps auxww) to show the complete command line.

### Solve
**Flag:** `pwn.college{EG5KVYPYu9E4MT-OQQg86k-UG9h.QX4MDO0wiN5AzNzEzW}`

Firstly, I checked for the commands ps,ps -ef, then ps -aux
then we have to find the file with the word challenge.

```bash
ps -efww
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 06:07 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7       1  0 06:07 ?        00:00:00 /run/dojo/bin/sleep 6h
root         132       1  0 06:07 ?        00:00:00 /challenge/14340-run-5822
root         135     132  0 06:07 ?        00:00:00 sleep 6h
hacker       146       1  0 06:07 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --port 7681 --interface 0.0.0.0 --writable -t disableLeaveAlert true /run/dojo/bin/bash --login
hacker       150     146  0 06:07 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       160       0  0 06:08 pts/1    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run/dojo/bin/ssh-entrypoint
hacker       166     160  0 06:08 pts/1    00:00:00 /run/dojo/bin/bash --login
hacker       178     166  0 06:11 pts/1    00:00:00 ps -efww
hacker@processes~listing-processes:~$ ps -efww | grep challenge
root         132       1  0 06:07 ?        00:00:00 /challenge/14340-run-5822
hacker       180     166  0 06:11 pts/1    00:00:00 grep --color=auto challenge
hacker@processes~listing-processes:~$ /challenge/14340-run-5822
Yahaha, you found me! Here is your flag:
pwn.college{EG5KVYPYu9E4MT-OQQg86k-UG9h.QX4MDO0wiN5AzNzEzW}
Now I will sleep for a while (so that you could find me with 'ps').
```

### New Learnings
ps -e anf ps aux both truncate the command. 

### References 
Add any references or videos you used while solving the challenge.
