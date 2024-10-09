# globbing matching
hacker@globbing~matching-with-:/bin$ cd
hacker@globbing~matching-with-:~$ /ch*
ssh-entrypoint: /challenge: Is a directory
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{QyPi4IvkUIh6LxpgbnlrPga93XC.dFjM4QDL3EzN0czW}
hacker@globbing~matching-with-:/challenge$ 


# matching with ?


hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{IykWsJiwyeh7JE4WOjgu6r4z3_M.dJjM4QDL3EzN0czW}

# matching with []
hacker@globbing~matching-with-:~$ cd challenge/files
ssh-entrypoint: cd: challenge/files: No such file or directory
hacker@globbing~matching-with-:~$ cd  /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run files_[bash]
Your expansion did not expand to the requested files (file_a, file_b, file_h, 
and file_s). Instead, it expanded to:
files_[bash]
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{sXq7lZdwGzPDCPrMJRGWG1gwUll.dNjM4QDL3EzN0czW}

# -piped-data-with-tee
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
Great job! Here is your flag:
pwn.college{IT85EvrwMRenHg_jADcdml3_Lug.dFjM5QDL3EzN0czW}


hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{QRUfFB6F7ifn7aggHVWTPgIUVQp.dRjM4QDL3EzN0czW}


# mixing globs 
hacker@globbing~mixing-globs:~$ cd /cha/*
ssh-entrypoint: cd: /cha/*: No such file or directory
hacker@globbing~mixing-globs:~$ /cha*
ssh-entrypoint: /challenge: Is a directory
hacker@globbing~mixing-globs:~$ cd /*ge/*s
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]
Your expansion did not expand to the requested files (challenging, educational, 
pwning). Instead, it expanded to:
[cep]
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{IQtLKpni-D8Y31accMADsmmaBM0.dVjM4QDL3EzN0czW}
hacker@globbing~mixing-globs:/challenge/files$ 

# exclusionary-globbing


hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run files[!wn]
Error: your argument is too long! It must be 8 characters or less.
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run file_[!pwn]*
Error: your argument is too long! It must be 8 characters or less.
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run file_[^pwn]*
Error: your argument is too long! It must be 8 characters or less.
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run_[!pwn]*
ssh-entrypoint: /challenge/run_[!pwn]*: No such file or directory
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{0vOukSXIMnhaW9y2WkNaQpD7VKo.dZjM4QDL3EzN0czW}


# writing-to-multiple-programs
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack |tee >(/challenge/the) | /challenge/planet
Congratulations, you have duplicated data into the input of two programs! Here 
is your flag:
pwn.college{8rKNoiBwXZqA407Ngy_kj8Q-k52.dBDO0UDL3EzN0czW}

# split-piping-stderr-and-stdout
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack 2> >( /challenge/the ) | /challenge/planet
Congratulations, you have learned a redirection technique that even experts 
struggle with! Here is your flag:
pwn.college{krfgR3nWlx5Z516YhLNvOnwBkzP.dFDNwYDL3EzN0czW}
