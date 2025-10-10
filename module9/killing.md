# Processes and Jobs

## Killing Processes
it's time to terminate your first process! In this challenge, 
/challenge/run will refuse to run while /challenge/dont_run is running!
You must find the dont_run process and kill it.
If you fail, pwn.college will disavow all knowledge of your mission. Good luck.

### Solve
**Flag:** `pwn.college{EoYGXf6iaTUzpistZsSB-uk9Lci.QXyQDO0wiN5AzNzEzW}`

Using ps -ef command to list the files using with | command and as told there will 
be dont_run file so grepped it. then killed the 136 file.

```bash
hacker@processes~killing-processes:~$ ps -ef | grep dont_run | grep -v grep
hacker       136     135  0 06:17 ?        00:00:00 /challenge/dont_run
hacker@processes~killing-processes:~$ kill 136
ps -ef | grep dont_run | grep -v grep || echo "dont_run terminated"
dont_run terminated
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{EoYGXf6iaTUzpistZsSB-uk9Lci.QXyQDO0wiN5AzNzEzW}
```

### New Learnings
Using Kill command .

### References 
Add any references or videos you used while solving the challenge.
