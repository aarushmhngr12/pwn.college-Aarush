# Pondering Paths 

## home sweet home 
Your argument must be an absolute path.
The path must be inside your home directory.
Before expansion, your argument must be three characters or less.
to get the absolute path. 

### Solve
**Flag:** `pwn.college{c5kmiSuzAcA2xV4v-vwcwKAgUPN.QXzMDO0wiN5AzNzEzW}`

giving an arguement to Linux and then we know that ~ is saved as home directory /home/hacker
then using ~ for it. 


```bash
echo LOOK: ~
/challenge/run ~/g
Writing the file to /home/hacker/g!
... and reading it back to you:
pwn.college{c5kmiSuzAcA2xV4v-vwcwKAgUPN.QXzMDO0wiN5AzNzEzW}
```

### New Learnings
learnt about saved sysmbol and giving the file.

### References 
Add any references or videos you used while solving the challenge.
