# Digesting Documents

## Help For Bulletins
Some commands, rather than being programs with man pages and help options, 
are built into the shell itself. These are called builtins. 
Builtins are invoked just like commands, but the shell handles them internally instead of launching other programs. 
You can get a list of shell builtins by running the builtin help. 

### Solve
**Flag:** `pwn.college{gXB0JXZC7hC68m-uBbRPC2igICO.QX0ETO0wiN5AzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "gXB0JXZC".
hacker@man~help-for-builtins:~$ challenge --secret gXB0JXZC
Correct! Here is your flag!
pwn.college{gXB0JXZC7hC68m-uBbRPC2igICO.QX0ETO0wiN5AzNzEzW}
```

### New Learnings
Using of help command in more complex situation.
### References 
Add any references or videos you used while solving the challenge.
