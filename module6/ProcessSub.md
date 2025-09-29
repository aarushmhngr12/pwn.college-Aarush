# Practicing Piping

## Process Substituion for input 
Use process substitution with diff to compare the outputs of these two programs and find your flag!

### Solve
**Flag:** `pwn.college{orkJhVkZ5H5Czc-5pTFjyRT-uyS.0lNwMDOxwiN5AzNzEzW}`

We already learnt the diff command and we used here the temporary file locactions to get the unmatched text line that containde the flag. 
``` bash
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
29a30
> pwn.college{orkJhVkZ5H5Czc-5pTFjyRT-uyS.0lNwMDOxwiN5AzNzEzW}
```

### New Learnings
Process Substitution

### References 
Add any references or videos you used while solving the challenge.
