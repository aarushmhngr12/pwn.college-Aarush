# Pondering Paths

## Position yet elsewhere 
Changing the directory after getting told by the command.

### Solve
**Flag:** `pwn.college{YOq74RB2JgRsvGksytOtaZYGSwz.QX4QTN0wiN5AzNzEzW}`

As written to type the initial command and it will show what to do, doing the same thing and aksing its abosulute path.

```bash
/challenge/run
Incorrect...
You are not currently in the /usr/share/doc directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /usr/share/doc
hacker@paths~position-yet-elsewhere:/usr/share/doc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{YOq74RB2JgRsvGksytOtaZYGSwz.QX4QTN0wiN5AzNzEzW}
```

### New Learnings
Brief note on what you learned from the challenge

### References 
Add any references or videos you used while solving the challenge.
