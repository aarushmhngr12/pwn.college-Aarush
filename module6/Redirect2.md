# Praticing Piping

## Redirecting More outputs
Aside from redirecting the output of echo, you can, of course, redirect the output of any command. 
In this level, /challenge/run will once more give you a flag,
but only if you redirect its output to the file myflag. 
Your flag will, of course, end up in the myflag file!

### Solve
**Flag:** `[FLAG] pwn.college{YERbLuAjfY7N2DI4o0J5Ez0dLym.QX1YTN0wiN5AzNzEzW}`

I ran the command for looking for myflag, it came out with information and then i read my file with cat.

```bash 
/challenge/run > myflag
hacker@piping~redirecting-more-output:~$ cat myflag
[FLAG] Here is your flag:
[FLAG] pwn.college{YERbLuAjfY7N2DI4o0J5Ez0dLym.QX1YTN0wiN5AzNzEzW}
```

### New Learnings
Redirecting output from a file by ike giving a path and using >.

### References 
Add any references or videos you used while solving the challenge.
