# Shell Variables

## Printing the Exported Variables
Try the env command: it'll print out every exported variable set in your shell, 
and you can look through that output to find the FLAG variable!

### Solve
**Flag:** `pwn.college{8DOCxIPgoSFv4JBdajVZw3UmUmI.QX4UTN0wiN5AzNzEzW}`

Using env to show up the list, then using env $FLAG.

```bash
env
env $FLAG
env: ‘pwn.college{8DOCxIPgoSFv4JBdajVZw3UmUmI.QX4UTN0wiN5AzNzEzW}’: Permission denied
```

### New Learnings
USing env Command to list up and get the flag.

### References 
Add any references or videos you used while solving the challenge.
