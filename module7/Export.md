# Shell Variable

## Exporting Variables
you must invoke /challenge/run with the PWN variable exported and set to the value COLLEGE,
and the COLLEGE variable set to the value PWN but not exported

### Solve
**Flag:** `pwn.college{wgtDNYr8EOKOQ1pE9rm6mtlvGl3.QXyYTN0wiN5AzNzEzW}`

Set the value of PWN to COLLEGE and export COLLEGE to PWN. and running it.

```bash
COLLEGE=PWN
 export PWN=COLLEGE
/challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great
job! Here is your flag:
pwn.college{wgtDNYr8EOKOQ1pE9rm6mtlvGl3.QXyYTN0wiN5AzNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
```

### New Learnings
The work of export command to set up tha variable value.

### References 
Add any references or videos you used while solving the challenge.
**
