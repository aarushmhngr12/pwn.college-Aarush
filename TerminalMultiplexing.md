# Terminal Multiplexing

## Launching Screen
launch screen

### Solve
**Flag** `pwn.college{0Oh6H321TRz0Ap1hX-qKRmZfDK2.0VN4IDOxwiN5AzNzEzW}`

```bash
screen
pwn.college{0Oh6H321TRz0Ap1hX-qKRmZfDK2.0VN4IDOxwiN5AzNzEzW}
```
### New Learnings
learned to launch screen

### Refrences
desrciption of the challenge



## Detaching and Attaching
launch screen detach run/challenge/run reattach screen

### Solve
**Flag** `  pwn.college{ARPBFrm_Qs_awnR52EA0_BAca31.0lN4IDOxwiN5AzNzEzW}`

```bash
screen
ctrl a then d
/challenge/run
screen -r
 pwn.college{ARPBFrm_Qs_awnR52EA0_BAca31.0lN4IDOxwiN5AzNzEzW}
```
### New Learnings
learned to detach and attach screen

### Refrences
desrciption of the challenge


## Finding Sessions
find the sessions reattach them to find the flag

### Solve
**Flag** `pwn.college{E8b3Sdk9LlV6V9SZpjKQaWkviQ_.01N4IDOxwiN5AzNzEzW}`

```bash
 screen -ls
There are screens on:
        144.session_f3aa1cdda2f09d15    (Detached)
        147.session_d275779227645ab0    (Detached)
        150.session_86edc3d0b2201875    (Detached)
3 Sockets in /home/hacker/.screen.
hacker@terminal-multiplexing~finding-sessions:~$  echo 'Congratulations! You found the right session!'
Congratulations! You found the right session!
hacker@terminal-multiplexing~finding-sessions:~$  echo pwn.college{E8b3Sdk9LlV6V9SZpjKQaWkviQ_.01N4IDOxwiN5AzNzEzW}
pwn.college{E8b3Sdk9LlV6V9SZpjKQaWkviQ_.01N4IDOxwiN5AzNzEzW}
hacker@terminal-multiplexing~finding-sessions:~$
```
### New Learnings
using screen -ls we can find all the sessions and their status 

### Refrences
desrciption of the challenge



## Switching Windows
find the flag in different windows 

### Solve
**Flag** `pwn.college{cpdEIGUzlbQn5sHJYA1ETj6bp_8.0FO4IDOxwSN0kjNzEzW}`

```bash
 screen -ls
There are screens on:
        144.session_f3aa1cdda2f09d15    (Remote or dead)
        150.session_86edc3d0b2201875    (Remote or dead)
        135.challenge_session   (Detached)
3 Sockets in /home/hacker/.screen.
hacker@terminal-multiplexing~switching-windows:~$ screen -r challenge_session
[detached from 135.challenge_session]
```
### New Learnings
ctrl A then 0-9 shows all the running windows in a session

### Refrences
desrciption of the challenge



## Detaching and Attaching tmux
Launch tmux
Detach from it.
Run /challenge/run (this will send the flag to your detached session!)
Reattach to see your prize

### Solve
**Flag** ` pwn.college{IXH7O_UP80L5oycNjAC74wt66ao.0VO4IDOxwiN5AzNzEzW}`

```bash
 tmux
[detached (from session 0)]
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ /challenge/run
Found detached tmux session: 0
Sending flag to your tmux session...

Flag sent! Now reattach to your tmux session with:
  tmux attach

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux a
[exited]
```
### New Learnings
instead of ctrl a we use ctrl b then d to detach and tmux a to attach 

### Refrences
desrciption of the challenge



## Switching windows tmux
switch to windows 0 insude the tmux session to get the flag

### Solve
**Flag** ` pwn.college{4SGIBy7Fv1e9lDqO9_wUXViSedb.0FM5IDOxwiN5AzNzEzW}`

```bash
 tmux ls
1: 1 windows (created Thu Oct  9 06:24:02 2025)
2: 1 windows (created Thu Oct  9 06:24:42 2025)
challenge_session: 2 windows (created Thu Oct  9 06:23:10 2025)
hacker@terminal-multiplexing~switching-windows-tmux:~$ tmux attach -t challenge_session
> Excellent work! You found window 0!
> Here is your flag: pwn.college{4SGIBy7Fv1e9lDqO9_wUXViSedb.0FM5IDOxwiN5AzNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{4SGIBy7Fv1e9lDqO9_wUXViSedb.0FM5IDOxwiN5AzNzEzW}
hacker@terminal-multiplexing~switching-windows-tmux:~$
```
### New Learnings
we can switch windowns inside a tmux session using ctrl b 0-9 

### Refrences
desrciption of the challenge
