# Praticinng Piping

## Redirecting Errors
Let's put this into practice! In this challenge, you will need to redirect the output of /challenge/run, 
like before, to myflag, and the "errors" (in our case, the instructions) to instructions. 
You'll notice that nothing will be printed to the terminal, because you have redirected everything! 
You can find the instructions/feedback in instructions and the flag in myflag when you successfully pull this off!

### Solve
**Flag:** `pwn.college{Ic_qLsol25KIEPsC12J71z0uJDg.QX3YTN0wiN5AzNzEzW}`

Using FDs to assigning and sending the errors to the intructions.

```bash
/challenge/run 1> myflag
/challenge/run 2> instructions
/challenge/run > myflag 2> instructions     #for sending the errors of myflag to instrcutions
cat myflag
[FLAG] Here is your flag:
[FLAG] pwn.college{Ic_qLsol25KIEPsC12J71z0uJDg.QX3YTN0wiN5AzNzEzW}

```

### New Learnings
Understanding different File Descriptor Numbers, like input,output,etc.


### References 
Add any references or videos you used while solving the challenge.
