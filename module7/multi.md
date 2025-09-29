# Shell Variables

## Multi-word Variables
the shell reads 1337 SAUCE as a single token,
and happily sets that value to VAR.
In this level, you'll need to set the variable PWN to COLLEGE YEAH.

### Solve
**Flag:** `pwn.college{Ea3iR5x2FKPseLV-eL49g86_CGu.QXwYTN0wiN5AzNzEzW}`

We have to use the " " to set the variable value to PWN.

```bash
 PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{Ea3iR5x2FKPseLV-eL49g86_CGu.QXwYTN0wiN5AzNzEzW}
```

### New Learnings
Setting up a variable using " ".
### References 
Add any references or videos you used while solving the challenge.
