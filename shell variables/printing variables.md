# printing variables
to get flag in this challenge we have to print the variable using echo command by prepending the variable with $
```bash
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{8NIzM7UIWIAW_BOTqE-uLVuowKf.ddTN1QDL0AjN0czW}
hacker@variables~printing-variables:~$
```
# setting variables
we have to set value of variable PWN to COLLEGE using "="
```bash
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{EHzDlZbwZorN_ofgIvmU-LuW0DP.dlTN1QDL0AjN0czW}
hacker@variables~setting-variables:~$
```

# Multi word variable
In thjs task we hae to gethe flag by declaring the variable PWN to COLLEGE YEAH by quoting the value COLLEGE YEAH 
```bash
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{k4sueLowyGmzq029T-QocumimMa.dBjN1QDL0AjN0czW}
hacker@variables~multi-word-variables:~$
```


# exporting variables 
here we have to run /challenge/run with the PWN variable exported and set to the value COLLEGE, and the COLLEGE variable set to the value PWN but it should not be exported 
```bash
Connected!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great
job! Here is your flag:
pwn.college{IRi81BzPAl1nNj6WBpaMQTG72Lp.dJjN1QDL0AjN0czW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
```

# printing exported variables 
In thistask we learn to useone more wa of printing variables in th previous tasks we used echo but here we'll use env 
```bash
Connected!
hacker@variables~printing-exported-variables:~$ env $FLAG
env: ‘pwn.college{wYe_NIgKTccVc9yRfl5CoTCpl9p.dhTN1QDL0AjN0czW}’
```

# storing command output
out flag is inside /challege/run so here we have to store the output ofthis command int th variable PWN usng the format VAR=$(fil_name)
```bash
Connected!
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{YeAJuY26GPczW4bcB1ACk5zXLgk.dVzN0UDL0AjN0czW}#
```

# READING INPUT
herrwe hae to use th command read to setbthe value of variable PWN to COLLEGE using read command which helps us reafinh theinput aong with -p wich specifies the prompt
```bash
Connected!
hacker@variables~reading-input:~$ read -p "INPUT: " PWN
INPUT: COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{MgdnY1k2Z0zNNhnI22iSR5isZB3.dhzN1QDL0AjN0czW}
```

# reading files 
```bash
Connected!
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{cCrFJWwuN9IlifOUuU954OKX1fP.dBjM4QDL0AjN0czW}
```
