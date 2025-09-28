# Practicing Piping

## Redirecting output
writing output of a command to a file

### Solve
**Flag:** `pwn.college{YOn2ySE2T9afoxeUEh-Y1nDSNtm.QX0YTN0wSOwAzNzEzW}`

use echo PWN > COLLEGE (> stores it in following filename)

```bash
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{YOn2ySE2T9afoxeUEh-Y1nDSNtm.QX0YTN0wSOwAzNzEzW}
```

### New Learnings
writing output of a file to a new file.

### References 
none

## Redirecting more output
writing output of a command to a file

### Solve
**Flag:** `pwn.college{UqQmtHoKmcmmuUIcGJkCXeNZVWV.QX1YTN0wSOwAzNzEzW}`

use challenge/run > myflag (> stores it in following filename)

```bash
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

[FLAG] Here is your flag:
[FLAG] pwn.college{UqQmtHoKmcmmuUIcGJkCXeNZVWV.QX1YTN0wSOwAzNzEzW}
```

### New Learnings
writing output of a any command to a new file.

### References 
none

## Appending output
Appending to already existing file

### Solve
**Flag:** `pwn.college{UqQmtHoKmcmmuUIcGJkCXeNZVWV.QX1YTN0wSOwAzNzEzW}`

/challenge/run >> ~/the-flag (>> appends already existing flag file)

```bash
hacker@piping~appending-output:~$ /challenge/run >> ~/the-flag
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
get the whole flag!
hacker@piping~appending-output:~$ cat the-flag 
 | 
\|/ This is the first half:
 v 
pwn.college{ELAueOelwBhn7FM3-z5eO8nrgnQ.QX3ATO0wSOwAzNzEzW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>) 
rather than *append* mode (>>), and so the write of the second half to stdout 
overwrote the initial write of the first half directly to the file. Try append 
mode!
```

### New Learnings
Appending to a file to save results of many commands in one output file.

### References 
none

## Redirecting errors
Redirecting standard errors to a file

### Solve
**Flag:** `pwn.college{UqQmtHoKmcmmuUIcGJkCXeNZVWV.QX1YTN0wSOwAzNzEzW}`

Use FD no 2 to write error to file

```bash
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2>instructions
hacker@piping~redirecting-errors:~$ cat myflag 

[FLAG] Here is your flag:
[FLAG] pwn.college{48lsbHl1f3wTVCVVdJzHOn14J3P.QX3YTN0wSOwAzNzEzW}
```

### New Learnings
Saving errors to a new file using FD numbers.

### References 
none

## Redirecting input
Redirecting input using <

### Solve
**Flag:** `pwn.college{ou9LeMC8X1J9nFjeLzYS_sIKuXg.QXwcTN0wSOwAzNzEzW}`

Use < to take input of a command from the file

```bash
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read 
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{ou9LeMC8X1J9nFjeLzYS_sIKuXg.QXwcTN0wSOwAzNzEzW}
```

### New Learnings
Redirecting input from other files into commands using <.

### References 
none

## Grepping stored results
Grepping flag from stored output

### Solve
**Flag:** `pwn.college{Mln121swDmyi4KTo8vx1BX1ICaw.QX4EDO0wSOwAzNzEzW}`

first write /chalenge/run to tmp/data.txt using > then grep pwn.college in it to get the flag.

```bash
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
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
hacker@piping~grepping-stored-results:~$ grep pwn.college /tmp/data.txt 
pwn.college{Mln121swDmyi4KTo8vx1BX1ICaw.QX4EDO0wSOwAzNzEzW}
```

### New Learnings
finding specific patterns from saved output file.

### References 
none

## Grepping live output
Using | to grep without creating file

### Solve
**Flag:** `pwn.college{sbgQRIlsCcCn-JuryCn5KvbcnG5.QX5EDO0wSOwAzNzEzW}`

/challenge/run | grep pwn.college . This the output of /challenge/run without creating output file.

```bash
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{sbgQRIlsCcCn-JuryCn5KvbcnG5.QX5EDO0wSOwAzNzEzW}
```

### New Learnings
finding specific patterns from output without saving it to a separate file.

### References 
none

## Grepping errors
Using >& to grep errors

### Solve
**Flag:** `pwn.college{w3jXdBF5PsBDRll6-DP5IcP3m2S.QX1ATO0wSOwAzNzEzW}`

2>& 1 writes the error to the standard output which is then grepped

```bash
hacker@piping~grepping-errors:~$ /challenge/run 2>& 1 | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{w3jXdBF5PsBDRll6-DP5IcP3m2S.QX1ATO0wSOwAzNzEzW}
```

### New Learnings
finding errors without saving it to a separate file.

### References 
Gemini explanation of 2> &1

## Filtering with grep -v
Using grep -v

### Solve
**Flag:** `pwn.college{ks0EFV04ISfyt6fgbqQkHyuJgX4.0FOxEzNxwSOwAzNzEzW}`

grep -v filters the data you dont want. It inverts grep command

```bash
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{ks0EFV04ISfyt6fgbqQkHyuJgX4.0FOxEzNxwSOwAzNzEzW}
```

### New Learnings
using grep -v to filter out unwanted patterns.

### References 
none

## Duplicating piped data with tee
Using tee

### Solve
**Flag:** `pwn.college{QzgxGWVsMRBXBHBK7il_5LdeS2M.QXxITO0wSOwAzNzEzW}`

/challenge/pwn output is piped using tee and help message is stored in output, this message is piped as input to /challenge/college but the command fails due to lack of secret data. Then read output to get the final command.

```bash
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee output | /challenge/college 
Processing...
WARNING: you are overwriting file output with tee's output...
The input to 'college' does not contain the correct secret code! This code 
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the 
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat output
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "QzgxGWVs"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret QzgxGWVs | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{QzgxGWVsMRBXBHBK7il_5LdeS2M.QXxITO0wSOwAzNzEzW}
```

### New Learnings
using tee to intercept data.

### References 
SENSAI,Gemini explanation of all commands

## Process substitution for input
Comparing output without saving file

### Solve
**Flag:** `pwn.college{Y3YNlMbKPetHPn7_0Bp8-FEO5Jf.0lNwMDOxwSOwAzNzEzW}`

use<()<() to run two commands and compare the outputs without saving output file

```bash
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/chal
lenge/print_decoys_and_flag) 
26a27
> pwn.college{Y3YNlMbKPetHPn7_0Bp8-FEO5Jf.0lNwMDOxwSOwAzNzEzW}
```

### New Learnings
using <() to run commands inside another command to avoid saving the file.

### References 
none

## Writing to multiple programs
Writing output of a command as input to two commands

### Solve
**Flag:** `pwn.college{Y3YNlMbKPetHPn7_0Bp8-FEO5Jf.0lNwMDOxwSOwAzNzEzW}`

use >() to pass output data as input to command

```bash
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) >(/challenge/planet)
This secret data must directly and simultaneously make it to /challenge/the and 
/challenge/planet. Don't try to copy-paste it; it changes too fast.
21963910420229925
Congratulations, you have duplicated data into the input of two programs! Here 
is your flag:
pwn.college{84QDPzpfyq-wA4fgVwcKC5CJwGH.QXwgDN1wSOwAzNzEzW}
```

### New Learnings
using >() to write output of a command to other commands.

### References 
SENSAI

## Split-piping sderr and stdout
Redirect stdout to one program and stderr to another

### Solve
**Flag:** `pwn.college{45mXGSLKwF2mZl1yseSauN0t66B.QXxQDM2wSOwAzNzEzW}`

use redirection and process substitution together. Pipe will not work as it only takes stdout.

```bash
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack  >(/challenge/hack) 2>(
/challenge/the) 
You must redirect my standard output into '/challenge/planet'!
It looks like you passed something like '>(something)' as an *argument* to 
/challenge/hack rather than redirecting /challenge/hack's out/error to 
'>(something)'. Remember, 'cmd1 >(cmd2)' does *NOT* redirect output of cmd1; 
rather, it'll run cmd2, hook a file up to its standard input, and pass that 
file as an argument to cmd1. If you want to redirect cmd1's output into that 
file, you will need to do: 'cmd1 > >(cmd2)', which is equivalent to 'cmd1 | 
cmd2'.
You must redirect my standard error into '/challenge/the'!
You must redirect my standard output into '/challenge/planet'!
You must redirect my standard error into '/challenge/the'!
Are you sure you're properly redirecting /challenge/hack's standard error into 
'/challenge/the'?
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack  >>(/challenge/hack) 2>
>(/challenge/the) 
bash: syntax error near unexpected token `('
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack  >> (/challenge/hack) 2
>> (/challenge/the) 
bash: syntax error near unexpected token `('
hacker@piping~split-piping-stderr-and-stdout:~$ ^C
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack  > >(/challenge/hack) 2
> >(/challenge/the) 
You must redirect my standard output into '/challenge/planet'!
You must redirect my standard error into '/challenge/the'!
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack  > >(/challenge/planet)
 2> >(/challenge/the) 
Congratulations, you have learned a redirection technique that even experts 
struggle with! Here is your flag:
pwn.college{45mXGSLKwF2mZl1yseSauN0t66B.QXxQDM2wSOwAzNzEzW}
```

### New Learnings
using piping to redirect stdout to one program and stderr to another program.

### References 
SENSAI,Gemini

## Named Pipes
Using custom made pipes

### Solve
**Flag:** `pwn.college{45mXGSLKwF2mZl1yseSauN0t66B.QXxQDM2wSOwAzNzEzW}`

create pipe and redirect the command output to it

```bash
hacker@piping~named-pipes:~$ cd /tmp/
hacker@piping~named-pipes:/tmp$ mkfifo flag_fifo
hacker@piping~named-pipes:/tmp$ /challenge/run > flag_fifo 
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo! 
Bash will now try to open the FIFO for writing, to pass it as the stdout of 
/challenge/run. Recall that operations on FIFOs will *block* until both the 
read side and the write side is open, so /challenge/run will not actually be 
launched until you start reading from the FIFO!
hacker@piping~named-pipes:~$ cat /tmp/flag_fifo 
You've correctly redirected /challenge/run's stdout to a FIFO at 
/tmp/flag_fifo! Here is your flag:
pwn.college{YLTfHtGU__uALSDMU6KjNj_ZNe-.01MzMDOxwSOwAzNzEzW}
```

### New Learnings
creating custom named pipes(file) so both commands are not required to be started at the same time as the file acts as a meeting point unlike | which is not saved in a file and deleted in memory after command execution.

### References 
SENSAI,Gemini explanation