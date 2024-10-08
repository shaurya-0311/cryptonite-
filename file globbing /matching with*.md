# matching with *
we use * to replace the rets of the agrument with any files that match that patter so we need to cd into challenge directory in less than 3 characters so we write cd/ch*
```bash
Connected!
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ ./run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{U2wZ65SUtaW2DaTZIGllp7SBTyp.dFjM4QDL0AjN0czW}
hacker@globbing~matching-with-:/challenge$
```

# Matching with 
? is used to match single character in the arguments therefore we used ? instead of c and l to cd into directory 
```bash
This challenge resets your working directory to /home/hacker unless you change
directory properly...
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ ./run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{Q66MK4iukoGEmUFx4u_nnztOn4H.dJjM4QDL0AjN0czW}
hacker@globbing~matching-with-:/challenge$
```

# Matching with []
The square brackes are, essentially, a limited form of ?, in that instead of matching any character, [] is a wildcard for some subset of potential characters so we make a single argument that bracket globs into the files file_b file_a file_s file_h
```bash
Connected!
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[absh]
You got it! Here is your flag!
pwn.college{4M21WLa8gr_bINdXVYRLVJxK0y5.dNjM4QDL0AjN0czW}
hacker@globbing~matching-with-:/challenge/files$
```

# matching paths with []
there are some files in /challenge/files and we have to start from our home directory and run /challenge/run with a single arhument that hglobs into absolute path of files file_b file_a file_s file_h
```bash
Connected!
hacker@globbing~matching-paths-with-:~$ cd ~
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{w8si5TZIpYFJxmQ0N1EE_xMxfu7.dRjM4QDL0AjN0czW}
hacker@globbing~matching-paths-with-:~$
```
# mixing globs 
using all the knowledge we've gained so far we use we have to write a single short glob less than equal to 6 characters that globs into files "challenging", "educational", and "pwning"
```bash
Connected!
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{kbhFzIKJ7zEX7aX_XfzyLD6Hkyp.dVjM4QDL0AjN0czW}
hacker@globbing~mixing-globs:/challenge/files$
```


# exclusionary-globbing

```bash
Connected!
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [^pwn]*
You got it! Here is your flag!
pwn.college{ItmCu6qo7MObkRbYZ0UALi1osvz.dZjM4QDL0AjN0czW}
hacker@globbing~exclusionary-globbing:/challenge/files$
```
