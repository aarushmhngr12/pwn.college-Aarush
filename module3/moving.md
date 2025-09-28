# Comprehending Commands

## Moving Files
This challenge wants you to move the /flag file into /tmp/hack-the-planet

### Solve
**Flag:** `pwn.college{M7aYul0OdbN4Z5lFWIwegqzmLM2.0VOxEzNxwiN5AzNzEzW}`

I thought to use the mv command from /flag to //tmp/hack-the-planet and then check the flag. 

```bash
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{M7aYul0OdbN4Z5lFWIwegqzmLM2.0VOxEzNxwiN5AzNzEzW}
```

### New Learnings
Moving one file to another.

### References 
Add any references or videos you used while solving the challenge.
