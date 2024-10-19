# Chaining with Semicolons
In this challenge, we learnt how to chain various commands using ;
```bash
Connected!
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn; /challenge/college
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{49dM1Pf-8TaqrXKfl2HR818tlMi.dVTN4QDL0AjN0czW}
```

# Your first shell script
In this challenge, we learnt to create a shell script ending with .sh suffix.
```bash
hacker@chaining~your-first-shell-script:~$ nano x.sh
hacker@chaining~your-first-shell-script:~$ chmod u+x x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{g9nBfjqQfgHxcT0MvvimJyTYmSS.dFzN4QDL0AjN0czW}
```

# Redirecting Script Output
In this challenge, we learnt how to redirect the script output and also the use of piping
```bash
hacker@chaining~redirecting-script-output:~$ nano x.sh
hacker@chaining~redirecting-script-output:~$ bash x.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{EHeXxD_3hYecjUMQTQN5D9EWNnG.dhTM5QDL0AjN0czW}
```

# Executable Shell Scripts
```bash
hacker@chaining~executable-shell-scripts:~$ nano solve_script.sh
hacker@chaining~executable-shell-scripts:~$ chmod +x solve_script.sh
hacker@chaining~executable-shell-scripts:~$ ./solve_script.sh
Congratulations on your shell script execution! Your flag:
pwn.college{kYNwC6yooFCW1lsCjC3i2qcjIz-.dRzNyUDL0AjN0czW}
```
