# Comprehending Commands

## More Catting Practice 
You cannot use the 'cd' command in this level, and must retrieve the flag by
absolute path. Plus, I hid the flag in a different directory!

### Solve
**Flag:** `pwn.college{8995aMroHkMS2I9xupVqRfFkjPZ.QXwITO0wiN5AzNzEzW}`

It was said not to use the cd to change directory, i used cat to read the files and accessed it and took out the flag. 
it was told that the file was in /lib/apt/solvers/flag.

```bash
cat /lib/apt/solvers/flag
pwn.college{8995aMroHkMS2I9xupVqRfFkjPZ.QXwITO0wiN5AzNzEzW}
```

### New Learnings
Accessing and Reading the flag in some other directory by using cat and by not changing the directories.

### References 
Add any references or videos you used while solving the challenge.
