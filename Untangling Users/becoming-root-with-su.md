# becoming-root-with-su
In this challenge, we learnt how to get root access using the su command
```bash
hacker@users~becoming-root-with-su:~$ su
Password:
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{8Jf0p6h05nADpEvA1SblTLm6W51.dVTN0UDL0AjN0czW}
root@users~becoming-root-with-su:/home/hacker#
```

# other users with su
```bash
Connected!
hacker@users~other-users-with-su:~$ su zardus
Password:
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{QMfGUchF-EybjPZIeQsvFbPyQ6c.dZTN0UDL0AjN0czW}
zardus@users~other-users-with-su:/home/hacker$
```

# cracking passwords
In this challenge, we learnt how to crack password for switching to the root user. This is done using John The Ripper tool. We do this, using the command john followed by the password list.
```bash
Connected!
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:20 100% 2/3 0.04914g/s 286.1p/s 286.1c/s 286.1C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password:
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{Q8Ud9-RDEA5jeB4tZO0lbgcdsXg.ddTN0UDL0AjN0czW}
```

# using sudo
In this challenge, we learnt the modification of su command, that is sudo
```bash
hacker@users~using-sudo:~$ sudo cat /flag
pwn.college{Yccsr1pq7Yac7ztkEHZzMRu0H5n.dhTN0UDL0AjN0czW}
```

