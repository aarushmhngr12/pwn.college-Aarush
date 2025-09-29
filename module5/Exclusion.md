# File Globbing

## Exclusionary Globbing
Armed with this knowledge, go forth to /challenge/files and run /challenge/run with all files that don't start with p, w, or n!
NOTE: The ! character has a different special meaning in bash when it's not the first character of a [] glob, 
so keep that in mind if things stop making sense! ^ does not have this problem, but is also not compatible with older shells.

### Solve
**Flag:** `pwn.college{4FX7rwmXknCAMS8SGNsvNlHfH1i.QX2IDO0wiN5AzNzEzW}`

Changing the directory and using glob [],! and *.

```bash
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files/
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{4FX7rwmXknCAMS8SGNsvNlHfH1i.QX2IDO0wiN5AzNzEzW}
hacker@globbing~exclusionary-globbing:/challenge/files$
```

### New Learnings
Brief note on what you learned from the challenge

### References 
Add any references or videos you used while solving the challenge.
