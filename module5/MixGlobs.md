# File Globbing

## Challenge Name
Go cd there and, using the globbing you've learned, write a single, short (6 characters or less) glob 
that (when passed as an argument to /challenge/run) will match the files "challenging", "educational", and "pwning"!

### Solve
**Flag:** `pwn.college{E3buV077-xvwO4R9-2p-Xbf6JyB.QX1IDO0wiN5AzNzEzW}`

First I changed the directory, i tried /challenge/run *[in]* but it showed me my mistake.
then i thought to see the list using ls command and then i pointed that c,p,e could be the one giving me the flag.
```bash
hacker@globbing~mixing-globs:/challenge/files$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run *[in]*
Your expansion did not expand to the requested files (challenging, educational,
pwning). Instead, it expanded to:
amazing beautiful challenging delightful educational fantastic incredible jovial kind laughing magical nice optimistic pwning queenly radiant splendid thrilling uplifting victorious wonderful xenial
hacker@globbing~mixing-globs:/challenge/files$ ls /challenge/files
amazing      delightful   great       jovial    magical     pwning   splendid   victorious  youthful
beautiful    educational  happy       kind      nice        queenly  thrilling  wonderful   zesty
challenging  fantastic    incredible  laughing  optimistic  radiant  uplifting  xenial
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{E3buV077-xvwO4R9-2p-Xbf6JyB.QX1IDO0wiN5AzNzEzW}
hacker@globbing~mixing-globs:/challenge/files$
```

### New Learnings
Using [] to find the multiple files at once.

### References 
Add any references or videos you used while solving the challenge.
