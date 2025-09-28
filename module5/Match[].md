# File GLobbing

## Matching with []
we will cover []. The square brackets are, essentially, a limited form of ?, in that instead of matching any character,
[] is a wildcard for some subset of potential characters, specified within the brackets.
For example, [pwn] will match the character p, w, or n.

### Solve
**Flag:** `pwn.college{EaJ1ns9d-2i9FyXZcwb5lCVdvKP.QXzIDO0wiN5AzNzEzW}`

Change the directory and run the command as given in example from where to where to run. 

```bash
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[absh]
You got it! Here is your flag!
pwn.college{EaJ1ns9d-2i9FyXZcwb5lCVdvKP.QXzIDO0wiN5AzNzEzW}
```

### New Learnings
Using of [] with the files inside the directory.

### References 
Add any references or videos you used while solving the challenge.
