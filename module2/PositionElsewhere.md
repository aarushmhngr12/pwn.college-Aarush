# Pondering Paths

## Position Elsewhere
To position your directory somewhere else. 
### Solve
**Flag:** `pwn.college{Avz1c2RxfY5y8hjfdVvj46H1ZSV.QX3QTN0wiN5AzNzEzW}`

Just like how we find out where the directory is in last question ,now the same but with diffeent directory and path. 

```bash
/challenge/run
Incorrect...
You are not currently in the /usr/aarch64-linux-gnu/include/gnu directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /usr/aarch64-linux-gnu/include/gnu
hacker@paths~position-elsewhere:/usr/aarch64-linux-gnu/include/gnu$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{Avz1c2RxfY5y8hjfdVvj46H1ZSV.QX3QTN0wiN5AzNzEzW}
```

### New Learnings
How to change the position elsewhere. 

### References 
Add any references or videos you used while solving the challenge.
