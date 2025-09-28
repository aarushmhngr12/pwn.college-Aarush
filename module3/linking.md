# Comprehending Commands

## Linking files 
In this level the flag is, as always, in /flag, but /challenge/catflag will instead read out /home/hacker/not-the-flag. Use the symlink, and fool it into giving you the flag!

### Solve
**Flag:** `pwn.college{waaabpHTxCluTiVWgVzRbrXmob1.QX5ETN1wiN5AzNzEzW}`

Linking the both the filesand then reading the given file.

```bash
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ cat /home/hacker/not-the-flag
cat: /home/hacker/not-the-flag: Permission denied
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{waaabpHTxCluTiVWgVzRbrXmob1.QX5ETN1wiN5AzNzEzW}
hacker@commands~linking-files:~$
```

### New Learnings
Linking Files and reading it from other files linked.

### References 
Add any references or videos you used while solving the challenge.
