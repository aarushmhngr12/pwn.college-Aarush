# Praticing Piping

## Redirecting Inputs
You can do interesting things with a lot of different programs using input redirection!
In this level, we will practice using /challenge/run, 
which will require you to redirect the PWN file to it and have the PWN file contain the value COLLEGE! 
To write that value to the PWN file, recall the prior challenge on output redirection from echo!


### Solve
**Flag:** `pwn.college{IumoOquJv39tOmtulowLoXUC2rP.QXwcTN0wiN5AzNzEzW}`

Firstly, echoing the PWN into the COLLEGE, then reading PWN resulting in COLLEGE, 
then using rev command to change into thte challenge files.
using challenge/run < rev giving out the input. 

``` bash 
echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ cat PWN
COLLEGE
rev < PWN
/challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{IumoOquJv39tOmtulowLoXUC2rP.QXwcTN0wiN5AzNzEzW}
```

### New Learnings
Using rev and < to redirect the user to the input. 

### References 
Add any references or videos you used while solving the challenge.
