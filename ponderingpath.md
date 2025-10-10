# Pondering PATH

## The PATH Variable 
Disrupt the operation of the /challenge/run program. This program will DELETE the flag file using the rm command. However, if it can't find the rm command, the flag will not be deleted, and the challenge will give it to you

### Solve
**Flag** `pwn.college{Us9ToyTE4BMup6X_OueT9oIArqO.QX2cDM1wiN5AzNzEzW}`

```bash
PATH=" "
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: command not found
The flag is still there! I might as well give it to you!
pwn.college{Us9ToyTE4BMup6X_OueT9oIArqO.QX2cDM1wiN5AzNzEzW}
```
### New Learnings
learned about PATH command. kept the path empty so that the rm could not be found upon rinning /challenge/run

### Refrences
desrciption of the challenge



## Setting Path
set path to the given directory and run /challenge/run

### Solve
**Flag** `pwn.college{kbLoIGskfZ_MsL_POC3hmA4XkFP.QX1cjM1wiN5AzNzEzW}`

```bash
hacker@path~setting-path:~$ PATH="/challenge/more_commands"
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{kbLoIGskfZ_MsL_POC3hmA4XkFP.QX1cjM1wiN5AzNzEzW}
```
### New Learnings
practiced more on path command

### Refrences
desrciption of the challenge



## Finding command
find the path of win command and cat flag

### Solve
**Flag** `pwn.college{QSxM0lJB1O9EyXZSt8n1czTL1w5.01NzEzNxwiN5AzNzEzW}`

```bash
which win
/challenge/paths/8792/win
hacker@path~finding-commands:~$ cat /challenge/paths/8792/win
#!/bin/bash

/bin/fold -s <<< "Search for the flag in the same directory in which I am located!"
hacker@path~finding-commands:~$ cd /challenge/paths/8792
hacker@path~finding-commands:/challenge/paths/8792$ cat win
#!/bin/bash

/bin/fold -s <<< "Search for the flag in the same directory in which I am located!"
hacker@path~finding-commands:/challenge/paths/8792$ cat flag
pwn.college{QSxM0lJB1O9EyXZSt8n1czTL1w5.01NzEzNxwiN5AzNzEzW}
```
### New Learnings
using which command we can find out the path of thst command

### Refrences
desrciption of the challenge



## Adding commands
make a shell script called win, add its location to the PATH, and enable /challenge/run to find it

### Solve
**Flag** `pwn.college{IsKBpmxxP2kmAs9pDaqNkBFEWX5.QX2cjM1wiN5AzNzEzW}`

```bash
 echo 'cat /flag' > win
hacker@path~adding-commands:~$ PATH=":$PATH"
hacker@path~adding-commands:~$ chmod a+x win
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
pwn.college{IsKBpmxxP2kmAs9pDaqNkBFEWX5.QX2cjM1wiN5AzNzEzW}
```
### New Learnings
adding commands while old commands stays the same

### Refrences
desrciption of the challenge


## Hijacking Commands
Again, this challenge will delete the flag using the rm command. But unlike before, it will not print anything out for you.
How can you solve this? You know that rm is searched for in the directories listed in the PATH variable. You have experience creating the win command when the previous challenge needed it.


### Solve
**Flag** `pwn.college{wnrHqQBhl9aODo-cYlRfv45mTw1.QX3cjM1wiN5AzNzEzW}`

```bash
hacker@path~hijacking-commands:~$ echo '#!/bin/bash' > /tmp/rm
hacker@path~hijacking-commands:~$ echo 'cat /flag' >> /tmp/rm
hacker@path~hijacking-commands:~$ chmod +x /tmp/rm
hacker@path~hijacking-commands:~$ export PATH="/tmp:$PATH"
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
Found 'rm' command at /tmp/rm. Executing!
pwn.college{wnrHqQBhl9aODo-cYlRfv45mTw1.QX3cjM1wiN5AzNzEzW}
```
### New Learnings
when /challenge/run invoked rm it found /tmp/rm before /bin/rm the actual rm file

### Refrences
desrciption of the challenge
