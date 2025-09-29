# Shell Variables

## StoringCommand Output
Now, you practice. Read the output of the /challenge/run command directly into a variable called PWN, and it will contain the flag!

### Solve
**Flag:** `pwn.college{k-amvPK_adIPcHW0MkVT6y44TQn.QX1cDN1wiN5AzNzEzW}`

As told we have to useCommand Substitution,

```bash
PWN=$( /challenge/run )
echo "$PWN"
pwn.college{k-amvPK_adIPcHW0MkVT6y44TQn.QX1cDN1wiN5AzNzEzW}
```

### New Learnings
Command Substitution.

### References 
Add any references or videos you used while solving the challenge.
