# Comprehending Commands

## Hidden Files 
Go find the flag, hidden as a dot-prepended file in /.

### Solve
**Flag:** `pwn.college{k99Ha-YtfJKnqr3BAzEixjw24R_.QXwUDO0wiN5AzNzEzW}`

Accesed to hidden files and got the dot prepended line and then read the line.

```bash
~$ ls -a /
.   .dockerenv             bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-134662822827830  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
$ cat /.flag-134662822827830
pwn.college{k99Ha-YtfJKnqr3BAzEixjw24R_.QXwUDO0wiN5AzNzEzW}
```

### New Learnings
Acccess to Hidden files.

### References 
Add any references or videos you used while solving the challenge.
