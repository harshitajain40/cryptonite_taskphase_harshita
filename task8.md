# LISTING PROCESSES

hacker@processes~listing-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  0.0   1056   640 ?        Ss   08:51   0:00 /sbin/docker-init -- /nix/var/nix/p
root           7  0.0  0.0   5052  2560 ?        S    08:51   0:00 /run/dojo/bin/sleep 6h
root          68  0.0  0.0   4132  2560 ?        S    08:51   0:00 /challenge/11167-run-32251
root          72  0.0  0.0   2744  1280 ?        S    08:51   0:00 sleep 6h
hacker        73  0.0  0.0   5360  3840 pts/0    Ss   08:51   0:00 /run/dojo/bin/ssh-entrypoint
hacker        93  0.0  0.0   7868  2880 pts/0    R+   09:10   0:00 ps aux
hacker@processes~listing-processes:~$ /challenge/11167-run-32251
Yahaha, you found me! Here is your flag:
pwn.college{Q0detNs9415cGGCmDNYWEyu_pDc.dhzM4QDL3EzN0czW}
Now I will sleep for a while (so that you could find me with 'ps').

# KILLING PROCESSES

hacker@processes~killing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 09:34 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bin/dojo-init /r
root           7       1  0 09:34 ?        00:00:00 /run/dojo/bin/sleep 6h
root          71       1  0 09:34 ?        00:00:00 su -c /challenge/.launcher hacker
hacker        73      71  0 09:34 ?        00:00:00 /challenge/dont_run
hacker        74      73  0 09:34 ?        00:00:00 sleep 6h
hacker        75       0  0 09:34 pts/0    00:00:00 /run/dojo/bin/ssh-entrypoint
hacker        92      75  0 09:34 pts/0    00:00:00 ps -ef
hacker@processes~killing-processes:~$ kill 73
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{o64Kt_JSevEoOUFelVuDA5YI43q.dJDN4QDL3EzN0czW}
hacker@processes~killing-processes:~$ 

# interrupting-processes

hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember, 
you can force me to exit with Ctrl-C. Try it now!
cccc^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{0cxk5gze5GZk-7eHZkE8sXikOS0.dNDN4QDL3EzN0czW}
hacker@processes~interrupting-processes:~$ 

 # suspending-processes
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root          82      65  0 15:30 pts/0    00:00:00 bash /challenge/run
root          84      82  0 15:30 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can 
background me with Ctrl-Z or, if you're not ready to do that for whatever 
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ run
ssh-entrypoint: run: command not found
hacker@processes~suspending-processes:~$ /run
ssh-entrypoint: /run: Is a directory
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root          82      65  0 15:30 pts/0    00:00:00 bash /challenge/run
root          91      65  0 15:31 pts/0    00:00:00 bash /challenge/run
root          93      91  0 15:31 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{o4oblivxg8BGe6ern5QbbsxCGh0.dVDN4QDL3EzN0czW}
hacker@processes~suspending-processes:~$ 


# resuming-processes
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with 
the 'fg' command! Or just press Enter to quit me!
^C
hacker@processes~resuming-processes:~$ ^C
hacker@processes~resuming-processes:~$ ^C
hacker@processes~resuming-processes:~$ ^C
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with 
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{AWPM1pDoPP9MRSx__x4pxRkgVdf.dZDN4QDL3EzN0czW}
Don't forget to press Enter to quit me!
 
Goodbye!



# backgrounding-processe

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



Yay, I'm now running the background! Because of that, this text will probably 
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
pwn.college{4XlY6_41fZstH2ayOMC7v6RXE4R.ddDN4QDL3EzN0czW}
hacker@processes~backgrounding-processes:~$ 





# foregrounding-processes
hacker@processes~foregrounding-processes:~$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the 
background, and *then* foreground it without re-suspending it! You can 
background me with Ctrl-Z (and resume me in the background with 'bg') or, if 
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[6]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg
[6]+ /challenge/run &



Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out. After that, resume me into the foreground with 'fg'; 
I'll wait.
hacker@processes~foregrounding-processes:~$ fg
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{ojUN3lY1WSCDtSuQDdBKrAEd6QT.dhDN4QDL3EzN0czW}
hacker@processes~foregrounding-processes:~$ 


# backgrounded-processes
hacker@processes~starting-backgrounded-processes:~$ /challenge/run
You've started me in the foreground! You must start me in the background (by 
appending '&' to the command) to get the flag!
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 85



Yay, you started me in the background! Because of that, this text will probably 
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{A0-1qk1uqO6G7CuKlvnXkxDP1Yx.dlDN4QDL3EzN0czW}
[1]+  Done                    /challenge/run
hacker@processes~starting-backgrounded-processes:~$ 



# processes~process-exit-codes
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ $?
ssh-entrypoint: 124: command not found
hacker@processes~process-exit-codes:~$ /challenge/submit-code 124
CORRECT! Here is your flag:
pwn.college{sMO4p-42J1KFu8zkMfNNpxx3IKi.dljN4UDL3EzN0czW}
hacker@processes~process-exit-codes:~$ 






