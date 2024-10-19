
# the-path-variable
hacker@path~the-path-variable:~$ PATH=""
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{kHshz8kifTa6UCIq378IVogdMyx.dZzNwUDL3EzN0czW}

# path setting path 
hacker@path~setting-path:~$ PATH=/challenge/more_commands/
hacker@path~setting-path:~$ cd /challenge/more_commands/
hacker@path~setting-path:/challenge/more_commands$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{Q9yUp-F8SQpKIDFC1rUl5I8K2sH.dVzNyUDL3EzN0czW}

# adding commands 
hacker@path~adding-commands:~$ which cat 
/run/workspace/bin/cat
hacker@path~adding-commands:~$ ls -l win
ls: cannot access 'win': No such file or directory
hacker@path~adding-commands:~$ ls -l win
ls: cannot access 'win': No such file or directory
hacker@path~adding-commands:~$ ls -l /run/workspace/bin/cat
lrwxrwxrwx 1 root root 17 Jan  1  1970 /run/workspace/bin/cat -> /run/dojo/bin/cat
hacker@path~adding-commands:~$ touch win
hacker@path~adding-commands:~$ ls -l win
-rw-r--r-- 1 hacker hacker 0 Oct 19 17:06 win
hacker@path~adding-commands:~$ chmod a+x win
hacker@path~adding-commands:~$ nano win
hacker@path~adding-commands:~$ export PATH=/home/hacker:$PATH
hacker@path~adding-commands:~$ echo $PATH
/home/hacker:/run/challenge/bin:/run/workspace/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
pwn.college{gKgqq9ACAySMr9z5md7b6EICvpl.dZzNyUDL3EzN0czW}
hacker@path~adding-commands:~$ 

