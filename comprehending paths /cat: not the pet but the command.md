# cat-not-the-pet-but-the-command
 cat is a command to read out the files so in order to get the flag we use cat command to read out the file "flag"
``` bash 
Connected!
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{EFuGou5TBD35E0UDNGIl8qGPpQ6.dFzN1QDL0AjN0czW}
```

# catting-absolute-paths
in the last we used cat command to read flag file in this we will read it using its absolute path taht is "/flag"
``` bash
Connected!
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{IPMxtzaTvMmD1H4YJEh18Az2B6B.dlTM5QDL0AjN0czW}
```

# More catting practice 
we can not use cd to change our directory therefore well use cat command and read the file directly through its absolute path 
``` bash
Connected!
You cannot use the 'cd' command in this level, and must retrieve the flag by
absolute path. Plus, I hid the flag in a different directory! You can find it
in the file /usr/lib/valgrind/flag. Go cat it out *without* cding into that
directory!
hacker@commands~more-catting-practice:~$ cat /usr/lib/valgrind/flag
pwn.college{Ysmoj9W9ZJYOwcJ--sa2J1Y1P97.dBjM5QDL0AjN0czW}
```

# Grepping for needle in a haystack 
greeping/grep is a command that is used to find files or lines of texts conatining SEARCH_STRING and prints them to the console, here we have to search flag in /challenge/data.txt and we know taht flag always starts with pwn.college 
``` bash
Connected!
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{k3leIW3TYlPjcTLSTHRt9cmbNuq.ddTM4QDL0AjN0czW}
```
# Listing files 
ls command is used for listing files in the directories provided to it as arguments. in the given task /challenge/run has been given a random name so we use ls command to list all the files in /challenge and find the file and run it 
``` bash hacker@commands~listing-files:~$ ls /challenge
6163-renamed-run-2261  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/6163-renamed-run-2261
Yahaha, you found me! Here is your flag:
pwn.college{kdL1SWESj5c81adl0ihxrDqMBA-.dhjM4QDL0AjN0czW}
hacker@commands~listing-files:~$
```

# Touching files 
touch command is used to create file. In this task we are required to make 2 files pwn and college and run /challenge/run in order to get the flag. so we first enter /tmp directory and create two files pwn and college and after creating the we run /challenge/run 
``` bash
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ ls
bin  college  hsperfdata_root  pwn  tmp.G9qthVCks5
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{g4tfKAHJaNHjA90MUTJXS5lljeh.dBzM4QDL0AjN0czW}
```

# Removing files 
to remove files we use the command rm. Given tasks tells us to create a delete_me file and then delete it. We first use touch command to create delete_me file and the use rm function to delete. In order to get the flag we run ?challenge/check 
```bash
Connected!
hacker@commands~removing-files:~$ touch delete_me
hacker@commands~removing-files:~$ ls
a  asd  delete_me  f  q  s
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ ls
a  asd  f  q  s
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{0QWtzbDvtZoLhVycE18baNnsFLM.dZTOwUDL0AjN0czW}
```

# Hidden files 
ls command whcih we used in the previous questions does not list all the files infact the file starting with '.' are not shown so in order to show those files we use ls -a command, once we identify the files we'll use cat command to list the flag in the file 
``` bash
hacker@commands~hidden-files:~$ ls -a
.  ..  .bash_history  .bash_logout  .bashrc  .profile  a  asd  f  q  s
hacker@commands~hidden-files:~$ ls -a /
.   .dockerenv            bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-27828132239727  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:~$ cat /.flag-27828132239727
pwn.college{460g1op_XQzk8UJOWv1RkdthqSD.dBTN4QDL0AjN0czW}
hacker@commands~hidden-files:~$
```

# making directories
we can make files using touch command , for making directories me use mkdir. The given task is to create a directory named "pwnn" and the create a file named "college". For makind directory we first enter /tmp using cd and then using mkdir we make our required directory and the enter to that directroy and using touch function we create the required file 
``` bash
hacker@commands~making-directories:~$ cd /tmp
hacker@commands~making-directories:/tmp$ mkdir pwn
hacker@commands~making-directories:/tmp$ ls
bin  hsperfdata_root  pwn  tmp.G9qthVCks5
hacker@commands~making-directories:/tmp$ cd pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ ls
college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{04YL30aNHdUMrR6MWycPUu3RpHz.dFzM4QDL0AjN0czW}
```


