# Pondering Paths

## Impilicit Relative Path from /
Using / find the cwd.

### Solve
**Flag:** `pwn.college{snLyD4yA-XJlky6gjpOZytoOHL0.QX5QTN0wiN5AzNzEzW}`

We got to know that use the shell bash /. then asking it directly challenge/run because it is current working directory.

```bash
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{snLyD4yA-XJlky6gjpOZytoOHL0.QX5QTN0wiN5AzNzEzW}
```

### New Learnings
Get to know the cwd function. 

### References 
Add any references or videos you used while solving the challenge.
