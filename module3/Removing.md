# Comprehending Commands

## Removing Files
Delete the iputed file delete_me and check for the flag. 

### Solve
**Flag:** `pwn.college{0483UuUclD3kNqbp-5wpp8e1Wzi.QX2kDM1wiN5AzNzEzW}`

As told that rm function work for deleting the file, so did it using rm delete_me and checked for it.

```bash
touch PWN
hacker@commands~removing-files:~$ touch college
hacker@commands~removing-files:~$ ls
PWN  college  delete_me  g
hacker@commands~removing-files:~$ rm PWN college delete_me
hacker@commands~removing-files:~$ ls
g
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{0483UuUclD3kNqbp-5wpp8e1Wzi.QX2kDM1wiN5AzNzEzW}}
```

### New Learnings
how to remove the files from the directory. 

### References 
Add any references or videos you used while solving the challenge.
