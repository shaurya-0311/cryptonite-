# The root
the file name starts with / so to invoke the programe our path would be /pwn
``` bash
hacker@paths~the-root:/$ /pwn
BOOM!!!
Here is your flag:
pwn.college{kQadlRlsCNrx9fRsSU6V9RT0N29.dhzN5QDL0AjN0czW}
```
# Program and absolute path 
the file we want to run is in /challenge directory so in order to run our "run" file pur code should be /challenge/run where /challenge is the directory in which our file is there and run is our required file 
``` bash
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{M0jW4YKcFkXjQ5LbNEx4C5xHSTz.dVDN1QDL0AjN0czW}
```

# Position thy self 
in order tu run our "/challenge/run" program we havr to change our cuurent directory to follow a particular path as in this case is /sys and then execute our code 
``` bash
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /sys directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /sys
hacker@paths~position-thy-self:/sys$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{AM9-THHhIe-4sWCink1t4TRMb2P.dZDN1QDL0AjN0czW}
```

# Position elsewhere
the working procedure is same as above the only difference is the path here is changed to we have cd into a new directory 
``` bash
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /
hacker@paths~position-elsewhere:/$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{EH5mlNAyrwWTZPAWocMfJapeLNe.ddDN1QDL0AjN0czW}
```

# Position yet elsewhere
again same as previous just have to cd into a different directory
```bash
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /tmp directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /tmp
hacker@paths~position-yet-elsewhere:/tmp$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{sHFvwlndG5qku9enENyOScfmPQ9.dhDN1QDL0AjN0czW}
```

# implicit-relative-paths-from /
here our cwd is "/" and we want to run /challenge/run using relative path so our relative path becomes "challenge/run" after we cd into "/"
``` bash
Connected!
hacker@paths~implicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{01e-r_PbdwYt5phTsjQtRtMns-7.dlDN1QDL0AjN0czW}
```

# explicit-relative-paths-from /
here our cwd is "/" and we have to run /challenge/run using explicit relative path using . so we chose any of the given paths listed 
``` bash
Connected!
hacker@paths~explicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the cd utility to change directory appropriately.
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{MfLxEapq1gQ7zCnWvHhTeFcZwVz.dBTN1QDL0AjN0czW}
hacker@paths~explicit-relative-paths-from-:/$
```

# implicit relative path 
to run "run" explicitly we tell linux system to explicitly want to execute a program in the current working directory 
``` bash
Connected!
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{0nEZodlFUoUphCNrvzLE2r35GRP.dFTN1QDL0AjN0czW}
```

# home sweet home 
in order to get the copy of the flag we make a path inside our hoem directory named as /q and use /challenge/run to get it
``` bash
Connected!
hacker@paths~home-sweet-home:~$ /challenge/run ~/q
Writing the file to /home/hacker/q!
... and reading it back to you:
pwn.college{oOqhjzfLpgSwLi98d-SxT59R7a5.dNzM4QDL0AjN0czW}
```
