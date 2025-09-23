# Pondering Paths

## Implicit Relative Paths
To tell Linux that you explicitly want to execute a program in the current directory, using .
### Solve
**Flag:** `pwn.college{IICTNK_IptAYnMH3ZthUEV61mg0.QXxUTN0wiN5AzNzEzW}`

Directly getting into the directory and then calling the command stating with '.' .

```bash
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ run
bash: run: command not found
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{IICTNK_IptAYnMH3ZthUEV61mg0.QXxUTN0wiN5AzNzEzW}
```

### New Learnings
Implicit Relative Path, it's relative path without using '/'.

### References 
Add any references or videos you used while solving the challenge.
