# Shell Variables

## Printing Variables
Print flag variable

### Solve
**Flag:** `pwn.college{4U7WrSu38Z_ztTmWnU30ozGHqOE.QX3UTN0wSOwAzNzEzW}`

use $ for variables

```bash
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{4U7WrSu38Z_ztTmWnU30ozGHqOE.QX3UTN0wSOwAzNzEzW}
```

### New Learnings
printing variables using $.

### References 
none

## Setting Variables
Set flag variable

### Solve
**Flag:** `pwn.college{cKIABtAx4NkZZgd2AOEwmsRNRIs.QX5UTN0wSOwAzNzEzW}`

set variables by using =

```bash
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{cKIABtAx4NkZZgd2AOEwmsRNRIs.QX5UTN0wSOwAzNzEzW}
```

### New Learnings
setting variables on terminal.

### References 
none

## Multi-word Variables
Set multi-word variable

### Solve
**Flag:** `pwn.college{EE3X6TleKtUyPxryCLgUCIbZHwA.QXwYTN0wSOwAzNzEzW}`

use "" for multi-word variables

```bash
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{EE3X6TleKtUyPxryCLgUCIbZHwA.QXwYTN0wSOwAzNzEzW}
```

### New Learnings
setting multi-word variables on terminal.

### References 
none

## Exporting Variables
Export variables to other commands

### Solve
**Flag:** `pwn.college{88meZwBVh6V3ET23GbobZTMvdg3.QXyYTN0wSOwAzNzEzW}`

use export

```bash
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great 
job! Here is your flag:
pwn.college{88meZwBVh6V3ET23GbobZTMvdg3.QXyYTN0wSOwAzNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
```

### New Learnings
exporting variables so they can be used by other shells as well.

### References 
none

## Printing Exported Variables
Print exported variables

### Solve
**Flag:** `pwn.college{IC8H16UyD90gSeVoP4tjUoIu1se.QX4UTN0wSOwAzNzEzW}`

use env command

```bash
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=7ce8ffb95c3a72e4940237876a9c1b8cc822e9371b4f1c58559b74e6d319d95d
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{IC8H16UyD90gSeVoP4tjUoIu1se.QX4UTN0wSOwAzNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
```

### New Learnings
using env command to print all exported variables set in your shell.

### References 
none

## Storing Command Output
Store output of other commands to a variable

### Solve
**Flag:** `pwn.college{0IRR35L15Nht7YRA-_8wEOLo_EK.QX1cDN1wSOwAzNzEzW}`

use $() to run command inside variable declaration command

```bash
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{0IRR35L15Nht7YRA-_8wEOLo_EK.QX1cDN1wSOwAzNzEzW}
```

### New Learnings
using command substitution $() to save output of other commands into a variable.

### References 
none

## Reading Input
Read inputted values in a variable

### Solve
**Flag:** `pwn.college{wCGCFoJlLwz6wrPaebhHuFRnKv7.QX4cTN0wSOwAzNzEzW}`

use read command 

```bash
hacker@variables~reading-input:~$ read -p "INPUT: " PWN
INPUT: COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{wCGCFoJlLwz6wrPaebhHuFRnKv7.QX4cTN0wSOwAzNzEzW}
```

### New Learnings
using read command to input and read upon setting of variable.

### References 
none

## Reading Files
Read from file

### Solve
**Flag:** `pwn.college{MeAyDguLuKUGsxPrDGZRVeKYdZy.QXwIDO0wSOwAzNzEzW}`

read the read_me file using PWN variable 

```bash
hacker@variables~reading-files:~$ read PWN < /challenge/read_me 
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{MeAyDguLuKUGsxPrDGZRVeKYdZy.QXwIDO0wSOwAzNzEzW}
```

### New Learnings
reading files with variables and without using cat to not run a whole other program.

### References 
none