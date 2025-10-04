# Data Manipulation    

## Extracting the first lines with head
/challenge/pwn outputs a bunch of data, and 
you'll need to pipe it through head to grab just the first 7 lines and 
then pipe them onwards to /challenge/college, 
which will give you the flag if you do this right! 
Your solution will be a long composite command with two pipes connecting three commands.

### Solve
**Flag:** `pwn.college{c6zkhHoZ8JMzqfQOJTp2tVnL4KJ.0lNxEzNxwiN5AzNzEzW}`

as we know we use add1 | add 2 to change the location.

```bash
/challenge/pwn | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{c6zkhHoZ8JMzqfQOJTp2tVnL4KJ.0lNxEzNxwiN5AzNzEzW}
```

### New Learnings
We learnt about the head command.'

### References 
Add any references or videos you used while solving the challenge.
