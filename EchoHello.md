# Hello Hackers
## Intro to Arguements 
When you type a line of text and hit enter, the shell actually parses your input into a command and its arguments. The first word is the command, and the subsequent words are arguments.
for example:
hacker@dojo:~$ echo Hello
Hello
hacker@dojo:~$
to get the flag, we have to run the hello command (NOT the echo command) with a single argument of hackers

### Solve
**Flag:** `pwn.college{kqzL7UlxInUXP_CtCL1sVOppUVs.QX4YjM1wiN5AzNzEzW}`

Firstly, Checking the command echo working properly or not, then after recheck with hello and hello hackers , I entered directly Hello Hackers to get the flag. 

```bash
echo hello
echo Hello Hackers!
hello hackers
```

### New Learnings
What I learnt is that how to echo the arguements and take out the flag for the challenge .

### References 
Add any references or videos you used while solving the challenge.
