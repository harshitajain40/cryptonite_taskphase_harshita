# chaining-with-semicolons
```
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn; /challenge/college
```
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{c7cNpVHQZZQmOP8uNWohQmWKXxn.dVTN4QDL3EzN0czW}


# chaining~your-first-shell-script
```
hacker@chaining~your-first-shell-script:~$ touch x.sh
hacker@chaining~your-first-shell-script:~$ nano x.sh 
hacker@chaining~your-first-shell-script:~$ bash x.sh
```
Great job, you've written your first shell script! Here is the flag:
pwn.college{sAfkA5EClWYcaVYbQQSABBAEFje.dFzN4QDL3EzN0czW}


# ~redirecting-script-output
```
hacker@chaining~redirecting-script-output:~$ nano x.sh
hacker@chaining~redirecting-script-output:~$ bash x.sh | /challenge/solve
```
Correct! Here is your flag:
pwn.college{Usrt3Eh6_bh-pOnJ0Di4AAmke6b.dhTM5QDL3EzN0czW}

# executable-shell-scripts
```
hacker@chaining~executable-shell-scripts:~$ ls -l x.sh
-rw-r--r-- 1 hacker hacker 35 Oct 19 12:55 x.sh
hacker@chaining~executable-shell-scripts:~$ chmod a=rwx x.sh
hacker@chaining~executable-shell-scripts:~$ ./x.sh
./x.sh: line 1: /challenge/pwn: No such file or directory
./x.sh: line 2: /challenge/college: No such file or directory
hacker@chaining~executable-shell-scripts:~$ neon x.sh
ssh-entrypoint: neon: command not found
hacker@chaining~executable-shell-scripts:~$ nano x.sh
hacker@chaining~executable-shell-scripts:~$ ./x.sh
```
Congratulations on your shell script execution! Your flag:
pwn.college{ob7-cFIyh5brRj4cW7l8TAX1YKb.dRzNyUDL3EzN0czW}
