# Digesting Documentation

## Learning From Documentation
basic documentation

### Solve
**Flag:** `pwn.college{0WbEUOIGYPI60Tvv62nvWtz0h0L.QX0ITO0wSOwAzNzEzW}`

use challenge/challenge --giveflag (given in documentation)

```bash
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{0WbEUOIGYPI60Tvv62nvWtz0h0L.QX0ITO0wSOwAzNzEzW}
```

### New Learnings
using documentation to give argument for flag

### References 
none

## Learning Complex Usage
complex documentation

### Solve
**Flag:** `pwn.college{otJ_5DvJEJWBfHCUZ-Xs7WC6Q2G.QX1ITO0wSOwAzNzEzW}`

use challenge/challenge/challenge --printfile /flag 

```bash
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag 
Correct argument! Here is the /flag file:
pwn.college{otJ_5DvJEJWBfHCUZ-Xs7WC6Q2G.QX1ITO0wSOwAzNzEzW}
```

### New Learnings
using complex documentation find flag using given argument

### References 
none

## Reading Manuals
man command

### Solve
**Flag:** `pwn.college{QM8_7K0CIQK2GnlOBRc0hiYsOjp.QX0EDO0wSOwAzNzEzW}`

use challenge/challenge/challenge --printfile /nlchis 870 (given in manual)

```bash
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --nlchis 870
Correct usage! Your flag: pwn.college{QM8_7K0CIQK2GnlOBRc0hiYsOjp.QX0EDO0wSOwAzNzEzW}
```

### New Learnings
using man command to learn about the challenge

### References 
none

## Searching Manuals
searching in man command

### Solve
**Flag:** `pwn.college{4I_j0BAVBtOnEWpmR_lMWn-S-x8.QX1EDO0wSOwAzNzEzW}`

use challenge/challenge/challenge --zy (search in man to get argument)

```bash
hacker@man~searching-manuals:~$ man challenge

gzip: stdout: Broken pipe
hacker@man~searching-manuals:~$ /challenge/challenge --zy
Initializing...
Correct usage! Your flag: pwn.college{4I_j0BAVBtOnEWpmR_lMWn-S-x8.QX1EDO0wSOwAzNzEzW}
hacker@man~searching-manuals:~$ 
```

### New Learnings
search operations in man command

### References 
none

## Searching For Manuals
advanced usage of man command

### Solve
**Flag:** `pwn.college{Aq_W88XK71rXMhNg2bvcYJFX4Hn.QX2EDO0wSOwAzNzEzW}`

find the argment to be used in man man, use -K argument to find hidden manpage where we get our argument for the flag.

```bash
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -K /challenge/challenge 
hacker@man~searching-for-manuals:~$ /challenge/challenge --qrhgbv 887
Correct usage! Your flag: pwn.college{Aq_W88XK71rXMhNg2bvcYJFX4Hn.QX2EDO0wSOwAzNzEzW}
```

### New Learnings
finding information from hidden manpages

### References 
SENSAI

## Helpful Programs
use of --help

### Solve
**Flag:** `pwn.college{AbZbB8dCtmP6AHCJflN4eat9bTL.QX3IDO0wSOwAzNzEzW}`

use /challenge/challenge --help and read how to get the flag.

```bash
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune]
                                            [-v]
                                            [-g GIVE_THE_FLAG]
                                            [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct
                        value
  -p, --print-value     print the value that will cause the
                        -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 864
hacker@man~helpful-programs:~$ /challenge/challenge -g 864
Correct usage! Your flag: pwn.college{AbZbB8dCtmP6AHCJflN4eat9bTL.QX3IDO0wSOwAzNzEzW}
```

### New Learnings
using --help to find information about programs without manpages

### References 
none

## Help for builtins
use of help for builtin commands

### Solve
**Flag:** `pwn.college{c9D_mKAyv2VJr2eELmhROGQ1IAV.QX0ETO0wSOwAzNzEzW}`

use help challenge as it is the builtin here and read the information to get the flag

```bash
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "c9D_mKAy".
hacker@man~help-for-builtins:~$ challenge --secret c9D_mKAy
Correct! Here is your flag!
pwn.college{c9D_mKAyv2VJr2eELmhROGQ1IAV.QX0ETO0wSOwAzNzEzW}
```

### New Learnings
using help for builtin commands like cd,ls etc.

### References 
none