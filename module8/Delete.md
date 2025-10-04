# Data Manipulation

## Deleting Characters
some decoy characters (specifically: ^ and %)
among the flag characters. Use tr -d to remove them!

### Solve
**Flag:** `pwn.college{oSBT0leHHDVzYL-cNHH6Du0z_t6.0FNxEzNxwiN5AzNzEzW}`

Using tr command in the /challenge/run to delete ^ and % .

```bash
/challenge/run | tr -d ^%
Your character-stuffed flag:
pwn.college{oSBT0leHHDVzYL-cNHH6Du0z_t6.0FNxEzNxwiN5AzNzEzW}
```

### New Learnings
Deleting characters using tr commands in any text.

### References 
Add any references or videos you used while solving the challenge.
