# Practicing Piping

## Writing to Multiple Programs
we have /challenge/hack, /challenge/the, and /challenge/planet. 
Run the /challenge/hack command, and duplicate its output as input to both the /challenge/the and the /challenge/planet commands! 

### Solve
**Flag:** `pwn.college{Mam3D2Ae8gZKRtg2glD0up69R_P.QXwgDN1wiN5AzNzEzW}`

As we had to duplicate the data to other files, we used tee and process substitution.

```bash
/challenge/hack | tee >( /challenge/the ) >( /challenge/planet )
This secret data must directly and simultaneously make it to /challenge/the and
/challenge/planet. Don't try to copy-paste it; it changes too fast.
2336180922751616838
Congratulations, you have duplicated data into the input of two programs! Here
is your flag:
pwn.college{Mam3D2Ae8gZKRtg2glD0up69R_P.QXwgDN1wiN5AzNzEzW}
```

### New Learnings
Duplicating usinf tee to the different file's input. 

### References 
Add any references or videos you used while solving the challenge.
