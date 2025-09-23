# Comprehending Commands

## Comparing Files
Use diff to find what's different between these files and get your flag

### Solve
**Flag:** `pwn.college{kHf2G3vAIlS_Lj8WiSeIXSe2YIC.01MwMDOxwiN5AzNzEzW}`

I showed up the cat the files first which gave me a lot of pwn.college flags and then i used 'diff' command to check which is differeing that will be our flag. 

```bash
$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
47a48
> pwn.college{kHf2G3vAIlS_Lj8WiSeIXSe2YIC.01MwMDOxwiN5AzNzEzW}
```

### New Learnings
Learnt about diff command

### References 
Add any references or videos you used while solving the challenge.
