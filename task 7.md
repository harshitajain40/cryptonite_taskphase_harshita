# printing variables 

hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{cFaqvB8aU1jEUoEoi6MPGjbn-NV.ddTN1QDL3EzN0czW}

# VARIABLE SETTING VARIABLE 
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{UOHUqc2UUfX3ZSmh1H9fgMSz0dN.dlTN1QDL3EzN0czW}

# MULTI WORD VARIABLE 
hacker@variables~multi-word-variables:~$ PWN=COLLEGE YEAH
bash: YEAH: command not found

It looks like you did not put quotes around the multi-word value in your 
variable assignment! This caused the shell to treat 'YEAH' as a command. Quote 
your multi-word values!
hacker@variables~multi-word-variables:~$ PWN='COLLEGE YEAH'
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{8TWFBOFQ-UMnkPoCulV-vMFOJM6.dBjN1QDL3EzN0czW}
hacker@variables~multi-word-variables:~$ 

# 

