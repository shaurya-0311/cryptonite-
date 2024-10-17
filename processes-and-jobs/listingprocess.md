# listing processes
/challenge/run file has been renamd with a ramdom name and we havr to ps ef and ps aux command to fnd it and run it 
```bash
hacker@processes~listing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 05:33 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bin/dojo-init /run/dojo/bin/sl
root           7       1  0 05:33 ?        00:00:00 /run/dojo/bin/sleep 6h
root          68       1  0 05:33 ?        00:00:00 /challenge/12416-run-18875
root          72      68  0 05:33 ?        00:00:00 sleep 6h
hacker        73       0  0 05:33 pts/0    00:00:00 /run/dojo/bin/ssh-entrypoint
hacker        92      73  0 05:33 pts/0    00:00:00 ps -ef
hacker@processes~listing-processes:~$  /challenge/12416-run-18875
Yahaha, you found me! Here is your flag:
pwn.college{AbdVHxND07NtJBVvrUnGBLkTrL9.dhzM4QDL0AjN0czW}
Now I will sleep for a while (so that you could find me with 'ps').
```

# killin-processes
here ee learn to kill a process with th hep of comman "kill" In this challenge, /challenge/run will refuse to run while /challenge/dont_run is running we have to find font run file and kill it 
```bashConnected!
hacker@processes~killing-processes:~$ ps -e
    PID TTY          TIME CMD
      1 ?        00:00:00 docker-init
      7 ?        00:00:00 /run/dojo/bin/s
     71 ?        00:00:00 su
     73 ?        00:00:00 bash
     74 ?        00:00:00 sleep
     75 pts/0    00:00:00 ssh-entrypoint
     92 pts/0    00:00:00 ps
hacker@processes~killing-processes:~$ kill 74
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{gwN4ZPeEouInzx3oMduny_HXTWy.dJDN4QDL0AjN0czW}
```

# intereptingbprocesses
some processes interupt the working of termina by clogging it therefore we have crtl+c command that sends an intereupt to the blocking command
```bash
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember,
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{U-DlY-5nPI4FIxkYZ4BwxPl6lXI.dNDN4QDL0AjN0czW}
```

# suspending processes 
we learnt above to use ctrl+c to interuot the blocking command byt here we will use crtl+z to suspend the process in the background
```bash
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root          82      65  0 05:43 pts/0    00:00:00 bash /challenge/run
root          84      82  0 05:43 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can
background me with Ctrl-Z or, if you're not ready to do that for whatever
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root          82      65  0 05:43 pts/0    00:00:00 bash /challenge/run
root          89      65  0 05:43 pts/0    00:00:00 bash /challenge/run
root          91      89  0 05:43 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{4u4OwNWzKFi93uAqikYoIu3jod_.dVDN4QDL0AjN0czW}
```

# resuming processes 
to resume the suspended process by crtl+z we use th command fg and puts it in the foreground of the terminal,this challenge's run needs you to suspend it, then resume it
```bash
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{wDNqUSDad9gMeDGo_IT0Msbg4qd.dZDN4QDL0AjN0czW}
Don't forget to press Enter to quit me!
```

# backgrouding processes
in the above task ee used fg to put the suspended command in the foreground but hre we will use bg command whivh will putbthe process in the background leaving the terminal open fir us to eroye more codes 
```bash
Connected!
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root          82 S+   bash /challenge/run
root          84 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the
background, and then launch a new version of me! You can background me with
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &



hacker@processes~backgrounding-processes:~$ Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out.

hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root          82 S    bash /challenge/run
root          92 S    sleep 6h
root          93 S+   bash /challenge/run
root          95 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{8hz3Fs2n7YxNwTwVrc2tdD_d2cj.ddDN4QDL0AjN0czW}
```

# foregroumding processes
```bash
Connected!
hacker@processes~foregrounding-processes:~$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the
background, and *then* foreground it without re-suspending it! You can
background me with Ctrl-Z (and resume me in the background with 'bg') or, if
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ pg
ssh-entrypoint: pg: command not found
hacker@processes~foregrounding-processes:~$ bg
[1]+ /challenge/run &



Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out. After that, resume me into the foreground with 'fg';
I'll wait.
hacker@processes~foregrounding-processes:~$ fg
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{g_Ajzc5qnJZOyzDhloLTmmpEcIV.dhDN4QDL0AjN0czW}
```

# starting background process 
to start the background process again we can use the command &  here sleep is actively running in the background, not suspended.launch /challenge/run
```bash
Connected!
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 82



Yay, you started me in the background! Because of that, this text will probably
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{k8Lg-VeQyPQ7FIcZeb6GrZ6tcDr.dlDN4QDL0AjN0czW}
[1]+  Done                    /challenge/run
hacker@processes~starting-backgrounded-processes:~$
```

# process exit codes 
every shell command including every program and every built in exits with an exit code when it finishes running and terminates we can see this code by using special varinale ?In this challenge, we have to retrieve the exit code returned by /challenge/get-code and then run /challenge/submit-code with that error code as an argument
```bash
Connected!
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
167
hacker@processes~process-exit-codes:~$ /challenge/submit-code 167
CORRECT! Here is your flag:
pwn.college{cw9bNgrslbpGXKzZrYPu6ej4G79.dljN4UDL0AjN0czW}
hacker@processes~process-exit-codes:~$
```
