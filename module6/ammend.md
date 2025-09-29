# Practicing Piping

## Appending Output
To practice, run /challenge/run with an append-mode redirect of the output to the file /home/hacker/the-flag. 
The practice will write the first half of the flag to the file, and the second half to stdout if stdout is redirected to the file. 
If you properly redirect in append-mode, the second half will be appended to the first,
but if you redirect in truncation mode (>), the second half will overwrite the first and you won't get the flag!

### Solve
**Flag:** `pwn.college{8oCComvpoe8BmkbFN-nnZEug-3l.QX3ATO0wiN5AzNzEzW}`

Using >> to get inside the file and appends it.
Entire flag will be transferred to the ~/the-flag.


```bash
/challenge/run >> /home/hacker/the-flag
cat /home/hacker/the-flag
 |
\|/ This is the first half:
 v
pwn.college{8oCComvpoe8BmkbFN-nnZEug-3l.QX3ATO0wiN5AzNzEzW}
                              ^
     that is the second half /|\
                              |
```

### New Learnings
Using >> to ammend the files. 

### References 
Add any references or videos you used while solving the challenge.
