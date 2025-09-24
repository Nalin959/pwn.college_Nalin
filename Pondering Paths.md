# Pondering Paths

## The Root
invoke program using command line

### Solve
**Flag:** `pwn.college{skRCnOTwVpvLrioMEr0zlODfLkb.QX4cTO0wSOwAzNzEzW}`

```bash
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{skRCnOTwVpvLrioMEr0zlODfLkb.QX4cTO0wSOwAzNzEzW}
```

### New Learnings
how to invoke program using command line
### References 
none

## Programs and Absolute paths
invoke program using absolute path

### Solve
**Flag:** `pwn.college{wXnBHft1N4kHmEKTY6UhhUuF0Fh.QX1QTN0wSOwAzNzEzW}`

```bash
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{wXnBHft1N4kHmEKTY6UhhUuF0Fh.QX1QTN0wSOwAzNzEzW}
```

### New Learnings
using absolute path
### References 
none

## Position thy self
set position using cd

### Solve
**Flag:** `pwn.college{0S6IsXX2xXKJ7ofMl2Ojp7VDSZy.QX2QTN0wSOwAzNzEzW}`

navigated to directory specified in challenge

```bash
hacker@paths~position-thy-self:/$ /challenge/run 
Incorrect...
You are not currently in the /var directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:/$ cd var
hacker@paths~position-thy-self:/var$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{0S6IsXX2xXKJ7ofMl2Ojp7VDSZy.QX2QTN0wSOwAzNzEzW}
```

### New Learnings
using cd to set your position
### References 
none

## Position elsewhere
navigate using cd

### Solve
**Flag:** `pwn.college{Ec4NUUoE_lEnyNLm7HpKImFEARZ.QX3QTN0wSOwAzNzEzW}`

navigated to directory specified in challenge

```bash
hacker@paths~position-elsewhere:~$ /challenge/run 
Incorrect...
You are not currently in the /usr/share/zoneinfo/posix/Asia directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd  /usr/share/zoneinfo/posix/Asia
hacker@paths~position-elsewhere:/usr/share/zoneinfo/posix/Asia$ /challenge/run 
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{Ec4NUUoE_lEnyNLm7HpKImFEARZ.QX3QTN0wSOwAzNzEzW}
```

### New Learnings
using cd to navigate through directories
### References 
none

## Position yet elsewhere
navigate using cd

### Solve
**Flag:** `pwn.college{YpkyAayH_wF6mCE8o3XU-OHUTlx.QX4QTN0wSOwAzNzEzW}`

navigated to directory specified in challenge

```bash
hacker@paths~position-yet-elsewhere:/$ /challenge/run 
Incorrect...
You are not currently in the /proc/138 directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:/$ cd /proc/138
hacker@paths~position-yet-elsewhere:/proc/138$ /challenge/run 
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{YpkyAayH_wF6mCE8o3XU-OHUTlx.QX4QTN0wSOwAzNzEzW}
```

### New Learnings
using cd to navigate through directories
### References 
none

## implicit relative paths,from /
using implicit relative paths

### Solve
**Flag:** `pwn.college{MLprpLnJR1wMGnIoblZeywzIzAQ.QX5QTN0wSOwAzNzEzW}`

navigated to / directory and use /challenge/run

```bash
hacker@paths~implicit-relative-paths-from-:/$ cd /
hacker@paths~implicit-relative-paths-from-:/$  challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{MLprpLnJR1wMGnIoblZeywzIzAQ.QX5QTN0wSOwAzNzEzW}
```

### New Learnings
using implicit relative paths from /
### References 
SENSAI

## explicit Relative Paths,from /
using explicit relative path

### Solve
**Flag:** `pwn.college{cZ3nJUHQNpnqB1p5D9a-vYKVE7g.QXwUTN0wSOwAzNzEzW}`

navigated to

```bash
hacker@paths~explicit-relative-paths-from-:/$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run 
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{cZ3nJUHQNpnqB1p5D9a-vYKVE7g.QXwUTN0wSOwAzNzEzW}
```

### New Learnings
using explicit relative paths from /

### References 
SENSAI

## implicit Relative Paths
using Implicit relative path

### Solve
**Flag:** `pwn.college{IBuhlQswTBJMGTzAxOfrzu_qV7d.QXxUTN0wSOwAzNzEzW}`

navigated to /challenge and use ./run

```bash
hacker@paths~implicit-relative-path:/challenge$ cd /challenge/
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{IBuhlQswTBJMGTzAxOfrzu_qV7d.QXxUTN0wSOwAzNzEzW}
```

### New Learnings
using Implicit relative paths to run programs. It will not run without using ./ as it is s safety feature of linux.

### References 
SENSAI

## home sweet home
using ~

### Solve
**Flag:** `pwn.college{QP0cLzA66COt8h5iOp3IEn61RQ2.QXzMDO0wSOwAzNzEzW}`

navigate to / , create new file using argument ~/a to copy the flag in a

```bash
hacker@paths~home-sweet-home:~$ cd /
hacker@paths~home-sweet-home:/$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{QP0cLzA66COt8h5iOp3IEn61RQ2.QXzMDO0wSOwAzNzEzW}
```

### New Learnings
use of ~ and writing flag to a new file specified in argument of /challegne/run

### References 
SENSAI

