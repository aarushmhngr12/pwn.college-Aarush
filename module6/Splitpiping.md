# Praticing Piping

## Split Piping strderr and stdout
You will need to combine your knowledge of >(), 2>, and |. How to do it is a task I'll leave to you.

### Solve
**Flag:** `pwn.college{o6RqjB1dAxxEaTG9B82dC26JQiz.QXxQDM2wiN5AzNzEzW}`

As we were told /challenge/hack stdout redirected /challenge/hack stdrr input.

```bash
/challenge/hack > >( /challenge/planet ) 2> >( /challenge/the )
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{o6RqjB1dAxxEaTG9B82dC26JQiz.QXxQDM2wiN5AzNzEzW}
```

### New Learnings
Combined Use of > ,>() and 2>.

### References 
Add any references or videos you used while solving the challenge.
