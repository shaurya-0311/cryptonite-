# learning from documentation 
we need to have proper documentation to run /challenge/challenge prgramme in this case it is by providing specifc arguments which is --giveflag
``` bash
Connected!
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{ozL8XYBOx0yU-VhVXI_SOQDCqmk.dRjM5QDL0AjN0czW}
hacker@man~learning-from-documentation:~$
```

# learning complex usage 
we can print all the arbitrary files when given the argument --printfile now the argument to printfiles argument will provide the path for flag 
``` bash
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{Y7To0AGPziR62NPu-QJyi6dupz7.dVjM5QDL0AjN0czW}
hacker@man~learning-complex-usage:~$
```

# Reading manuals 
we use man function to read into challenge and then we find a suitable argument that gibes us the flag 
``` bash
hacker@man~reading-manuals:~$ /challenge/challenge --kitdac 162
Correct usage! Your flag: pwn.college{kiEtdHBQHXaRMX1c6L-aER2ZQhN.dRTM4QDL0AjN0czW}
hacker@man~reading-manuals:~
```
# Searching manuals 
we use man feature to read /challenge/challenge and find the suitable argument using the / function to search. we can search keywords like "flag" 
```bash
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --muxcl
Initializing...
Correct usage! Your flag: pwn.college{MrqsE3PjWrJ3JPWre3PAcCzayjL.dVTM4QDL0AjN0czW}
hacker@man~searching-manuals:~$
```

# Helpful programs 
we use --help argument to see all the arguments and chose the right one among those. as we can see in the folloeing code
```bash
Connected!
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 619
hacker@man~helpful-programs:~$ /challenge/challenge -g 619
Correct usage! Your flag: pwn.college{EZupdQZTnyX6u1K9U_sKQ0VC7nk.ddjM4QDL0AjN0czW}
hacker@man~helpful-programs:~$
```

# help fot builtins 
we use the command help challenge to and see whats inside and then proceed as indicated 
```bash
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "sV2G1-U6".
hacker@man~help-for-builtins:~$ challenge --secret sV2G1-U6
Correct! Here is your flag!
pwn.college{sV2G1-U6X-breNOjmbb9AfnQDHO.dRTM5QDL0AjN0czW}
```


