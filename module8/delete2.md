# Data Manipulation

## Deleting Newlines
we'll inject a bunch of newlines into the flag.
Delete them with tr's -d flag and the escaped newline specification!

### Solve
**Flag:** `pwn.college{4KPr3lainaWKd9Dw4NqgHjFamx-.0VNxEzNxwiN5AzNzEzW}`

As we know the function of command echo, it recalls it again and again.
using echo it makes the command easier for us.

```bash
/challenge/run | tr -d '\n' echo
tr: extra operand ‘echo’
Only one string may be given when deleting without squeezing repeats.
Try 'tr --help' for more information.
/challenge/run | tr -d '\n'; echo
Your line-split flag: pwn.college{4KPr3lainaWKd9Dw4NqgHjFamx-.0VNxEzNxwiN5AzNzEzW}
```

### New Learnings
Using tr to delete the newlines.

### References 
Add any references or videos you used while solving the challenge.
