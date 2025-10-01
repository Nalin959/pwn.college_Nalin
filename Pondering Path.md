# Pondering Paths

## The PATH variable
Use PATH variable

### Solve
**Flag:** `pwn.college{sauStQKBj3W4IjPU4GJbwJJJNum.QX2cDM1wSOwAzNzEzW}`

set path variable blank so rm cannot be found

```bash
hacker@path~the-path-variable:~$ rm
rm: missing operand
Try 'rm --help' for more information.
hacker@path~the-path-variable:~$ PATH=''
hacker@path~the-path-variable:~$ /challenge/run 
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{sauStQKBj3W4IjPU4GJbwJJJNum.QX2cDM1wSOwAzNzEzW}
```

### New Learnings
PATH variable is responsible for finding commands which stores a bunch of directory paths in which the shell will search for programs corresponding to commands. 

### References 
none

## Setting PATH
Set PATH variable

### Solve
**Flag:** `pwn.college{o4HT2RJcHWjBJyPo-qNxqA3a_rN.QX1cjM1wSOwAzNzEzW}`

set path variable to command location

```bash
hacker@path~setting-path:~$ PATH=/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run 
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{o4HT2RJcHWjBJyPo-qNxqA3a_rN.QX1cjM1wSOwAzNzEzW}
```

### New Learnings
PATH variable can be set to command location. 

### References 
none

## Finding Commands
Find commands using which

### Solve
**Flag:** `pwn.college{Y21ZmFTEmOCjCbMEqE9vcGytXYa.01NzEzNxwSOwAzNzEzW}`

use which

```bash
hacker@path~finding-commands:~$ which win
/challenge/paths/32706/win
hacker@path~finding-commands:~$ cat /challenge/paths/32706/flag
pwn.college{Y21ZmFTEmOCjCbMEqE9vcGytXYa.01NzEzNxwSOwAzNzEzW}
```

### New Learnings
using which to find command location. 

### References 
none

## Setting PATH
Set PATH variable

### Solve
**Flag:** `pwn.college{o4HT2RJcHWjBJyPo-qNxqA3a_rN.QX1cjM1wSOwAzNzEzW}`

set path variable to command location

```bash
hacker@path~setting-path:~$ PATH=/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run 
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{o4HT2RJcHWjBJyPo-qNxqA3a_rN.QX1cjM1wSOwAzNzEzW}
```

### New Learnings
PATH variable can be set to command location. 

### References 
none

## Adding Commands
Add commands to PATH

### Solve
**Flag:** ``

use which

```bash

```

### New Learnings
 

### References 
