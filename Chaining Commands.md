# Chaining Commands

## Chaining with Semicolons
Chain commands using ;

### Solve
**Flag:** `pwn.college{s0i3Os92w8WEZ_HzYuA-nDjcUqo.QX1UDO0wSOwAzNzEzW}`

use ; to run the commands one after the other

```bash
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn ; /challenge/college 
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{s0i3Os92w8WEZ_HzYuA-nDjcUqo.QX1UDO0wSOwAzNzEzW}
```

### New Learnings
chaining commands to make them run the in order with just one prompt.

### References 
none

## Building on Success
Run second command if first succeds

### Solve
**Flag:** `pwn.college{c88hKeo16EivkKOVmAEx2ymuOT1.0lM0MDOxwSOwAzNzEzW}`

use && operator

```bash
hacker@chaining~building-on-success:~$ /challenge/first-success && /challenge/second 
Nice chaining! Flag: pwn.college{c88hKeo16EivkKOVmAEx2ymuOT1.0lM0MDOxwSOwAzNzEzW}
```

### New Learnings
running second command only if first command succeeds.

### References 
none

## Handling Failure
Run second command if first fails

### Solve
**Flag:** `pwn.college{QDlsvRfAoJXJIzwIMGE2i7AGAS3.01M0MDOxwSOwAzNzEzW}`

use || operator

```bash
hacker@chaining~handling-failure:~$ /challenge/first-failure || /challenge/second 
Nice chaining! Flag: pwn.college{QDlsvRfAoJXJIzwIMGE2i7AGAS3.01M0MDOxwSOwAzNzEzW}
```

### New Learnings
running second command only if first command fails.

### References 
none

## Your first shell script
Run shell script

### Solve
**Flag:** `pwn.college{squR2_0Qoo8DBtKtxdGIh_-lzes.QXxcDO0wSOwAzNzEzW}`

create .sh file, write commands and use bash to run them

```bash
hacker@chaining~your-first-shell-script:~$ cd ~
hacker@chaining~your-first-shell-script:~$ bash x.sh 
Great job, you've written your first shell script! Here is the flag:
pwn.college{squR2_0Qoo8DBtKtxdGIh_-lzes.QXxcDO0wSOwAzNzEzW}
```

### New Learnings
using shell scripts to run a file with saved commands.

### References 
none

## Redirecting Script Output
Redirect script output to another command

### Solve
**Flag:** `pwn.college{YvzA_IKi2V0YjSS869R5QKkuZ1o.QX4ETO0wSOwAzNzEzW}`

pipe sh command to /challenge/solve

```bash
hacker@chaining~redirecting-script-output:~$ bash x.sh | /challenge/solve 
Correct! Here is your flag:
pwn.college{YvzA_IKi2V0YjSS869R5QKkuZ1o.QX4ETO0wSOwAzNzEzW}
```

### New Learnings
Redirecting shell scripts output using pipe.

### References 
none

## Executable Shell Scripts
Make shell scripts executable

### Solve
**Flag:** `pwn.college{UIwcmQRcYSDUX0qdsog9qaaPth6.QX0cjM1wSOwAzNzEzW}`

change execute permission using chmod then run .sh file

```bash
hacker@chaining~executable-shell-scripts:~$ ls ~/x.sh -la
-rw-r--r-- 1 hacker hacker 16 Oct  1 16:46 /home/hacker/x.sh
hacker@chaining~executable-shell-scripts:~$ chmod a+x ~/x.sh 
hacker@chaining~executable-shell-scripts:~$ ./x.sh
Congratulations on your shell script execution! Your flag:
pwn.college{UIwcmQRcYSDUX0qdsog9qaaPth6.QX0cjM1wSOwAzNzEzW}
```

### New Learnings
Making shell scripts executable so we don't have to use bash.

### References 
none

## Understanding Shebangs
Using Shebangs

### Solve
**Flag:** `pwn.college{YU-May0umHX5Q7lrVILLG85Evw2.0VOzMDOxwSOwAzNzEzW}`

change execute permissions using chmod and write #!/bin/bash in first line of solve.sh file

```bash
hacker@chaining~understanding-shebangs:~$ chmod a+x solve.sh 
hacker@chaining~understanding-shebangs:~$ /challenge/run 
Testing your script...
Perfect! Your flag:
Flag: pwn.college{YU-May0umHX5Q7lrVILLG85Evw2.0VOzMDOxwSOwAzNzEzW}
```

### New Learnings
Using shebangs so that other programs can run the shell script(earlier only bash could run it).

### References 
none

## Scripting with Arguments
Using arguments in scripts.

### Solve
**Flag:** `pwn.college{kNAmy-stKe4deA6JnEimJ1qsUbN.0VNzMDOxwSOwAzNzEzW}`

write echo "$2 $1" to give second argument first then second

```bash
hacker@chaining~scripting-with-arguments:~$ /challenge/run 
Correct! Your script properly reversed the arguments.
Here's your flag:
pwn.college{kNAmy-stKe4deA6JnEimJ1qsUbN.0VNzMDOxwSOwAzNzEzW}
```

### New Learnings
using arguments in shell scripts.

### References 
none

## Scripting with Conditionals
Using conditionals in scripts.

### Solve
**Flag:** `pwn.college{g0FWMXbyLGeErz7TFGZxcwgylHS.0lNzMDOxwSOwAzNzEzW}`

use if then fi statement as shown in challenge description 

```bash
hacker@chaining~scripting-with-conditionals:~$ /challenge/run 
Correct! Your script properly handles all the conditions.
Here's your flag:
pwn.college{g0FWMXbyLGeErz7TFGZxcwgylHS.0lNzMDOxwSOwAzNzEzW}
```

### New Learnings
using conditionals in shell scripts.

### References 
none

## Scripting with Default cases
Using conditionals with default cases in scripts.

### Solve
**Flag:** `pwn.college{Er2wsDxwgVNj0P98u3GpTnE1_5r.01NzMDOxwSOwAzNzEzW}`

use if then else fi statement as shown in challenge description 

```bash
hacker@chaining~scripting-with-default-cases:~$ /challenge/run 
Correct! Your script properly handles the if/else conditions.
Here's your flag:
pwn.college{Er2wsDxwgVNj0P98u3GpTnE1_5r.01NzMDOxwSOwAzNzEzW}
```

### New Learnings
using conditionals with default cases(else) in shell scripts.

### References 
none

## Scripting with Multiple Conditions
Using multiple conditionals in scripts.

### Solve
**Flag:** `pwn.college{oZ6j9e4Zoj7RJQ3LkdKXBdmJk8t.0FOzMDOxwSOwAzNzEzW}`

use if then elif else fi statement as shown in challenge description 

```bash
hacker@chaining~scripting-with-multiple-conditions:~$ /challenge/run 
Correct! Your script properly handles all the conditions with elif.
Here's your flag:
pwn.college{oZ6j9e4Zoj7RJQ3LkdKXBdmJk8t.0FOzMDOxwSOwAzNzEzW}
```

### New Learnings
using multiple conditionals with default cases(else) in shell scripts.

### References 
none

## Reading Shell Scripts
Read shell scripts.

### Solve
**Flag:** `pwn.college{cv084w-snLZr570IYXlugyQeryd.0lMwgDOxwSOwAzNzEzW}`

use cat to read script then use password 

```bash
hacker@chaining~reading-shell-scripts:~$ cat /challenge/run 
#!/opt/pwn.college/bash

read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
        echo "CORRECT! Your flag:"
        cat /flag
else
        echo "Read the /challenge/run file to figure out the correct password!"
fi
hacker@chaining~reading-shell-scripts:~$ /challenge/run 
hack the PLANET
CORRECT! Your flag:
pwn.college{cv084w-snLZr570IYXlugyQeryd.0lMwgDOxwSOwAzNzEzW}
```

### New Learnings
Reading shell scripts using cat.

### References 
none