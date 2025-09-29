# Praticing Piping

## Named Pipes
his challenge will be a simple introduction to FIFOs. You'll need to create a /tmp/flag_fifo file and
redirect the stdout of /challenge/run to it. If you're successful, /challenge/run will write the flag into the FIFO! Go do it!

### Solve
**Flag:** `pwn.college{IPUhLJpd-3rNpqjhq29N_ZkLTV8.01MzMDOxwiN5AzNzEzW}`

as the nature of fifo wants two terminals to operate.

```bash
 mkfifo /tmp/flag_fifo  (T1)
 cat /tmp/flag_fifo (T1)
/challenge/run > /tmp/flag_fifo (T2)
You've correctly redirected /challenge/run's stdout to a FIFO at
/tmp/flag_fifo! Here is your flag:
pwn.college{IPUhLJpd-3rNpqjhq29N_ZkLTV8.01MzMDOxwiN5AzNzEzW} (T1)
```

### New Learnings
FIFO

### References 
Add any references or videos you used while solving the challenge.
