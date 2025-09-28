# Hello Hackers

## Intro to Commands 
the user executed the whoami command, which simply prints the username (hacker) to the terminal. When the command terminates, the shell once again displays the prompt, ready for the next command.
So, invoke the hello command to get the flag!

### Solve
**Flag:'pwn.college{YjIN2qN-NfrUEy9-WZe0qdk3fg6.QX3YjM1wiN5AzNzEzW}'** `pwn.college{helloworld}`

First to connect to hacker@dojo server which make us into the hacker@intro-to-the-commands and when we typed hello specifically, it must show Success and the flag.
```bash
ssh -i key hacker@dojo.pwn.college
hello
pwn.college{helloworld}
```

### New Learnings
What I learnt is that how to connect to the server for the challenges and how to output the flag. 

### References 
Github and pwn.college
