# File Globbing

## Matching with *
The first glob we'll learn is *. When it encounters a * character in any argument, the shell will treat it as a "wildcard" and try to replace that argument with any files that match the pattern

### Solve
**Flag:** `pwn.college{YHmetPwoe-mKj0Io2oulzKzVQzA.QXxIDO0wiN5AzNzEzW}`

As said to write in less than 4, i used /c*.

```bash
hacker@globbing~matching-with-:~$ cd /c*
/challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{YHmetPwoe-mKj0Io2oulzKzVQzA.QXxIDO0wiN5AzNzEzW}
```

### New Learnings
USing of * command.

### References 
Add any references or videos you used while solving the challenge.
