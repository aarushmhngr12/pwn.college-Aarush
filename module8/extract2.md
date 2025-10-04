# Data manipulation 

## Extracting specific sections from text
the /challenge/run program will give you a bunch of lines with random numbers and
single characters (characters of the flag) as columns. 
Use cut to extract the flag characters, then pipe them to tr -d "\n" 
(like the previous level!) to join them together into a single line.

### Solve
**Flag:** `pwn.college{M6HVXKWhhzHZta2-dWAGbuZe5hd.01NxEzNxwiN5AzNzEzW}`

Thought about the number where to start, so ran /challenge/run it showed me to use it from 2
used it from 2 and also added the command to pipe them together.

```bash
 /challenge/run | cut -d ' ' -f 2 | tr -d '\n'
pwn.college{M6HVXKWhhzHZta2-dWAGbuZe5hd.01NxEzNxwiN5AzNzEzW}
```

### New Learnings
cut command to extract things from different sections of text.

### References 
Add any references or videos you used while solving the challenge.
