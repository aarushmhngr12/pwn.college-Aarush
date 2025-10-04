# Data Manipulation 

## Translating Characters 
challenge/run will print the flag but will swap the casing of all characters
(e.g., A will become a and vice-versa). 


### Solve
**Flag:** `pwn.college{MJP5j9--eyezb4Vcb0MhvIK-SCx.01MxEzNxwiN5AzNzEzW}`

As we were told to change every letter case so i though of taking it together in a string thing.


```bash
/challenge/run | tr a-z A-Z | tr A-Z a-z
your case-swapped flag:
pwn.college{mjp5j9--eyezb4vcb0mhvik-scx.01mxeznxwin5aznzezw}
```

### New Learnings
We can change the letter of any text using tr command.

### References 
Add any references or videos you used while solving the challenge.
