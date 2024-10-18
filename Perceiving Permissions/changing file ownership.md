# chaging file ownership 
here we'll use chown command to change the ownership of the /flag file which is currently set to root but we'll change it to hackr so that we can get the flag
```bash
hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{I7If2wetRD1AOzjR2TkmFhMSaua.dFTM2QDL0AjN0czW}
```

# groups and fils 
here we have to change group of the file using chgrp command snce thehackeris neither root user or root group so the file is not accessible so we use chgrp
```
hacker@permissions~groups-and-files:~$ chgrp hacker /flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{YC-lSXf9VXgzmg0WSvhq5JkvUPp.dFzNyUDL0AjN0czW}
```

# fun with group names 
here our user has been changed to a random name and we have to use id command to find out the uder and then use chgrp command 
```bash
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp13334) groups=1000(grp13334)
hacker@permissions~fun-with-groups-names:~$ chgrp grp13334 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{Iw5T7KgRUm_BFe2gcf_F_5fr4dL.dJzNyUDL0AjN0czW}
```

# changong perissions 
here file /flag is not made readable to us therefre we must chmod command along with u+r to make it readable,a+r adds read access to the user's permissions
```bash
hacker@permissions~changing-permissions:~$ chmod a+r /flag
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{0TU_WSxz63jQs3jkVkRDeCSbcRl.dNzNyUDL0AjN0czW}
hacker@permissions~changing-permissions:~$
```

# executable files
```
hacker@permissions~executable-files:~$ chmod u+x /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
Successful execution! Here is your flag:
pwn.college{EHJjIMblgxuO0N4hu2CWBDK8dM7.dJTM2QDL0AjN0czW}
hacker@permissions~executable-files:~$
```

#
