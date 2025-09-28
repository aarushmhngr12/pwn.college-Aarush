# Comprehending Paths

## Listing Files
To list the files and taking out flag from another directory.

### Solve
**Flag:** `pwn.college{8rE4WNrRjDtnSSy0ZKCpPLy4mU_.QX4IDO0wiN5AzNzEzW}`

Firstly as told used /challenge, which showed me a renamed file which was obviously the text file , then wrote it off to find the flag.

```bash
ls /challenge
12969-renamed-run-9365  DESCRIPTION.md
grep flag /challenge/12969-renamed-run-9365
echo "Yahaha, you found me! Here is your flag:"
cat /flag
/challenge/12969-renamed-run-9365
Yahaha, you found me! Here is your flag:
pwn.college{8rE4WNrRjDtnSSy0ZKCpPLy4mU_.QX4IDO0wiN5AzNzEzW}
```

### New Learnings
Listing of files.

### References 
Add any references or videos you used while solving the challenge.
