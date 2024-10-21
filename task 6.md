
# redirecting output
```
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
```
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your 
flag:
pwn.college{MkDDP_kwgIHNlNnKGYctguzXI2d.dRjN1QDL3EzN0czW}

# redirecting more output 
```
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag
```
[FLAG] Here is your flag:
[FLAG] pwn.college{Y9LuRUpWP-dVZhgYfq7erziWw9f.dVjN1QDL3EzN0czW}

# appending output
```
hacker@piping~appending-output:~$ /challenge/run >> /home/hacker/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!

[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do 
the first write directly to the file, and the second write, I'll do to stdout 
(if it's pointing at the file). If you redirect the output in append mode, the 
second write will append to (rather than overwrite) the first write, and you'll
```
get the whole flag!

 | 


#redorecting error 
```
hacker@piping~redirecting-errors:~$ /challenge/run 1> myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat instructions
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will check that error output is redirected to a specific file path : instructions
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!

[TEST] You should have redirected my stderr to instructions. Checking...

[PASS] The file at the other end of my stderr looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-errors:~$ cat myflag
```
[FLAG] Here is your flag:
[FLAG] pwn.college{sr3RxBrMUBAlFqRtIn69UWqotKV.ddjN1QDL3EzN0czW} 



# REDIRECTING INPUT 
```
hacker@piping~redirecting-input:~$ /challenge/run > PWN 
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN 
hacker@piping~redirecting-input:~$ cat PWN
COLLEGE
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read 
the value 'COLLEGE' out of it!
```
Here is your flag:
pwn.college{ECi_9GWVhpMbvwQpn46oQ7cntNn.dBzN1QDL3EzN0czW}

# grepping-stored-results
```
hacker@piping~grepping-stored-results:~$ /challenge/run >  /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep "flag" /tmp/data.txt
[FLAG] Here is your flag:
flagging
flagstone
flagstones
flagellation
flagellating
flagrantly
camouflages
unflagging
conflagrations
flagrant
flagella
flagon
flagpole
flagpole's
conflagration
flagged
flagpoles
flag's
flagship's
flagellum's
flagellated
persiflage
flagstaffs
camouflage's
flagon's
camouflaged
flagstaff's
flagship
flagellates
flagellate
flag
flagellums
flagons
conflagration's
flagstone's
flagellum
flagships
flagstaff
camouflage
flagellation's
persiflage's
camouflaging
flags
hacker@piping~grepping-stored-results:~$ grep pwn.colleg /tmp/data.txte
grep: /tmp/data.txte: No such file or directory
hacker@piping~grepping-stored-results:~$ grep pwn.colleg /tmp/data.txt
```
pwn.college{gHcwNJvOWSCBYAo0XAgY3Fw8g08.dhTM4QDL3EzN0czW}




# grepping-live-output
```
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/xpq4yhadyhazkcsggmqd7rsgvxb3kjy4-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
```
pwn.college{sBgUS8OR5Z4V6pAigz-NMC6axQf.dlTM4QDL3EzN0czW}


# grepping-errors
```
hacker@piping~grepping-errors:~$ /challenge/run 2>& 1 | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/xpq4yhadyhazkcsggmqd7rsgvxb3kjy4-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
```
pwn.college{45N0tZLvk8ASmhOsQ2XG4O-6fRK.dVDM5QDL3EzN0czW}


# -piped-data-with-tee
```
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code 
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the 
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee pwn_output | /challenge/college
Processing...
WARNING: you are overwriting file pwn_output with tee's output...
The input to 'college' does not contain the correct secret code! This code 
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the 
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat pwn_output
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "IT85Evrw"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret IT85Evrw | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
```
Great job! Here is your flag:
pwn.college{IT85EvrwMRenHg_jADcdml3_Lug.dFjM5QDL3EzN0czW}



# duplicating-piped-data-with-tee
```
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee pwn_output | /challenge/college
Processing...
WARNING: you are overwriting file pwn_output with tee's output...
The input to 'college' does not contain the correct secret code! This code 
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the 
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat pwn_output
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "IT85Evrw"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret IT85Evrw | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
```
Great job! Here is your flag:
pwn.college{IT85EvrwMRenHg_jADcdml3_Lug.dFjM5QDL3EzN0czW}



# writing-to-multiple-programs
```
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack |tee >(/challenge/the) | /challenge/planet
Congratulations, you have duplicated data into the input of two programs! Here
```
is your flag:
pwn.college{8rKNoiBwXZqA407Ngy_kj8Q-k52.dBDO0UDL3EzN0czW}

# split-piping-stderr-and-stdout
```
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack 2> >( /challenge/the ) | /challenge/planet
Congratulations, you have learned a redirection technique that even experts
```
struggle with! Here is your flag:
pwn.college{krfgR3nWlx5Z516YhLNvOnwBkzP.dFDNwYDL3EzN0czW}
