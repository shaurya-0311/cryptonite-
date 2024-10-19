# Pondering PATH
In this challenge, we learnt the concept of PATH variable which consists of bunch of directory paths in which shell will search for programs corresponding to commmands
```bash
hacker@path~the-path-variable:~$  PATH=''
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{wB_nCanelkPNkIxHjHdx9HGllJc.dZzNwUDL0AjN0czW}
```

# Setting PATH
In this challenge, we learnt how to add custom path to the PATH variable to obtain useful results
```bash
Connected!
hacker@path~setting-path:~$ PATH='/challenge/more_commands/'
hacker@path~setting-path:~$ /challenge/run win
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{84q2zD0m-Ob6lCIFbcwp5NGWaI2.dVzNyUDL0AjN0czW}
hacker@path~setting-path:~$
```

# Adding Commands
```bash
hacker@path~adding-commands:~$ nano win
hacker@path~adding-commands:~$ ls
COLLEGE  PWN  asd       f             intercepted_data    myfile  not-the-flag  s          solve_script.sh  test      win
Desktop  a    data.txt  instructions  intercepted_output  myflag  q             script.sh  temp.txt         the-flag  x.sh
hacker@path~adding-commands:~$ ./win
ssh-entrypoint: ./win: Permission denied
hacker@path~adding-commands:~$ chmod +x win
hacker@path~adding-commands:~$ echo $PATH
/run/challenge/bin:/run/workspace/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
hacker@path~adding-commands:~$ PATH='/home/hacker'
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
pwn.college{41SATMovCiMsOEnZVz1v6mZC9aT.dZzNyUDL0AjN0czW}
```

# Hijacking Commands
```bash
hacker@path~hijacking-commands:~$ rm
rm: missing operand
Try 'rm --help' for more information.
hacker@path~hijacking-commands:~$ nano rm
hacker@path~hijacking-commands:~$ chmod +x rm
hacker@path~hijacking-commands:~$ PATH='/home/hacker'
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
pwn.college{stfY-5d-vRy_XwI6jBAmHk5k7Ed.ddzNyUDL0ITO0czW}
```

