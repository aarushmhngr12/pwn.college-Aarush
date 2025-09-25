# Comprehending Files

## Making Directories
Making a directory, then creating a college file and checking its run.

### Solve
**Flag:** `pwn.college{EsOpsrSaH0RzOuFbs9bg6sQUWCC.QXxMDO0wiN5AzNzEzW}`

Created the directory , inputted the file and rechecked it.

```bash
hacker@commands~making-directories:~$ cd /tmp
hacker@commands~making-directories:/tmp$ mkdir pwn
hacker@commands~making-directories:/tmp$ ls
bin  hsperfdata_root  pwn  tmp.TpSOPGOVKK
hacker@commands~making-directories:/tmp$ cd pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{EsOpsrSaH0RzOuFbs9bg6sQUWCC.QXxMDO0wiN5AzNzEzW}
hacker@commands~making-directories:/tmp/pwn$

```

### New Learnings
Making Directories

### References 
Add any references or videos you used while solving the challenge.
