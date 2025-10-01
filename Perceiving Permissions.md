# Perceiving Permissions

## Changing File Ownership
Change file ownership to hacker

### Solve
**Flag:** `pwn.college{ozQp1YhnkOb8aCB8s4O5Uc15tby.QXxEjN0wSOwAzNzEzW}`

use chown to change owner

```bash
hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ cat /flag 
pwn.college{ozQp1YhnkOb8aCB8s4O5Uc15tby.QXxEjN0wSOwAzNzEzW}
```

### New Learnings
changing ownership of a file in terminal.

### References 
PWN College videos

## Groups and Files
Change group to hacker

### Solve
**Flag:** `pwn.college{01pXgjPEWAvN0ELoerEfQwUUOU8.QXxcjM1wSOwAzNzEzW}`

use chgrp

```bash
hacker@permissions~groups-and-files:~$ ls -la /flag 
-r--r----- 1 root root 60 Oct  1 14:06 /flag
hacker@permissions~groups-and-files:~$ chgrp hacker /flag 
hacker@permissions~groups-and-files:~$ cat /flag 
pwn.college{01pXgjPEWAvN0ELoerEfQwUUOU8.QXxcjM1wSOwAzNzEzW}
```

### New Learnings
changing group of a file in terminal.

### References 
PWN College videos

## Fun with group names
Change group to hacker(group name is different)

### Solve
**Flag:** `pwn.college{AM3O5fszQ4Fi_EmgXFhXZUFp-Yw.QXycjM1wSOwAzNzEzW}`

use id to get group name and chgrp to change group

```bash
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp5170) groups=1000(grp5170)
hacker@permissions~fun-with-groups-names:~$ chgrp grp5170 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{AM3O5fszQ4Fi_EmgXFhXZUFp-Yw.QXycjM1wSOwAzNzEzW}
```

### New Learnings
finding group names then change file group.

### References 
PWN College videos

## Changing Permissions
Change permission using chmod

### Solve
**Flag:** `pwn.college{014HKx6uQrhURvo7soKl6F1IVgW.QXzcjM1wSOwAzNzEzW}`

use chmod a+rw to give read and write permission to all users

```bash
hacker@permissions~changing-permissions:~$ ls -la /flag 
-r-------- 1 root root 60 Oct  1 14:36 /flag
hacker@permissions~changing-permissions:~$ chmod a+rw /flag 
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{014HKx6uQrhURvo7soKl6F1IVgW.QXzcjM1wSOwAzNzEzW}
```

### New Learnings
changing permissions of file or directory.

### References 
PWN College videos

## Executable files
Change permission using chmod to execute files

### Solve
**Flag:** `pwn.college{M3QdZekVL7RAWsSVhkCOHF-UTGq.QXyEjN0wSOwAzNzEzW}`

use chmod a+x to give execute permission

```bash
hacker@permissions~executable-files:~$ ls /challenge/run -la 
-r--r--r-- 1 hacker hacker 32 Jan 14  2025 /challenge/run
hacker@permissions~executable-files:~$ chmod a+x /challenge/run 
hacker@permissions~executable-files:~$ /challenge/run 
Successful execution! Here is your flag:
pwn.college{M3QdZekVL7RAWsSVhkCOHF-UTGq.QXyEjN0wSOwAzNzEzW}
hacker@permissions~executable-files:~$ 
```

### New Learnings
changing permissions to execute programs.

### References 
PWN College videos

## Permission Tweaking Practice
Practice change permissions using chmod

### Solve
**Flag:** `pwn.college{QylU8OpgGr4d5D_7ZAu1PAH5htx.QXwEjN0wSOwAzNzEzW}`

use chmod to change permissions as required

```bash
hacker@permissions~permission-tweaking-practice:~$ /challenge/run 
Round 1 of 8!

Current permissions of "/challenge/pwn": rw-r--r--
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rw-r--rw-
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod o+w /challenge/pwn
You set the correct permissions!
Round 2 of 8!

Current permissions of "/challenge/pwn": rw-r--rw-
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": ---------
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod a-rwx /challenge/pwn 
You set the correct permissions!
Round 3 of 8!

Current permissions of "/challenge/pwn": ---------
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": ------r--
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod o+r /challenge/pwn 
You set the correct permissions!
Round 4 of 8!

Current permissions of "/challenge/pwn": ------r--
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": r--r--r--
* the user does have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod a+r /challenge/pwn 
You set the correct permissions!
Round 5 of 8!

Current permissions of "/challenge/pwn": r--r--r--
* the user does have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": r--r-xr--
* the user does have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod g+x /challenge/pwn 
You set the correct permissions!
Round 6 of 8!

Current permissions of "/challenge/pwn": r--r-xr--
* the user does have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rwxrwxrwx
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod a+rwx /challenge/pwn 
You set the correct permissions!
Round 7 of 8!

Current permissions of "/challenge/pwn": rwxrwxrwx
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": rwxrwx-w-
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
* the world does have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod o-rx /challenge/pwn 
You set the correct permissions!
Round 8 of 8!

Current permissions of "/challenge/pwn": rwxrwx-w-
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
- the world doesn't have read permissions
* the world does have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rwxr-----
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod g-wx,o-rwx /challenge/pwn 
You set the correct permissions!
You've solved all 8 rounds! I have changed the ownership
of the /flag file so that you can 'chmod' it. You won't be able to read
it until you make it readable with chmod!

Current permissions of "/flag": ---------
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod a+r /flag 
hacker@permissions~permission-tweaking-practice:~$ cat /flag
pwn.college{QylU8OpgGr4d5D_7ZAu1PAH5htx.QXwEjN0wSOwAzNzEzW}
```

### New Learnings
changing permissions execute programs.

### References 
PWN College videos

## Permission Setting Practice
Setting permission using chmod

### Solve
**Flag:** `pwn.college{cIyZu7i12wrwCa8gEbRDF3g_Bxw.QXzETO0wSOwAzNzEzW}`

use chmod and set a,g,o using = to set permissions rather than changing it

```bash
hacker@permissions~permissions-setting-practice:~$ /challenge/run 
Round 1 of 8!

Current permissions of "/challenge/pwn": rw-r--r--
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rw------x
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
* the world does have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod a=rw,g=-,o=x /challenge/pwn 
You set the correct permissions!
Round 2 of 8!

Current permissions of "/challenge/pwn": rw------x
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": rwxrw-rwx
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod a=rwx,g=rw,o=rwx /challenge/pwn 
You set the correct permissions!
Round 3 of 8!

Current permissions of "/challenge/pwn": rwxrw-rwx
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": ---r---w-
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
* the world does have write permissions
- the world doesn't have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod a=-,g
=r,o=w /challenge/pwn 
You set the correct permissions!
Round 4 of 8!

Current permissions of "/challenge/pwn": ---r---w-
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
* the world does have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": ----w---x
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
* the world does have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod a=-,g=w,o=x /challenge/pwn 
You set the correct permissions!
Round 5 of 8!

Current permissions of "/challenge/pwn": ----w---x
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": ----w-rwx
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod a=-,g=w,o=rwx /challenge/pwn 
You set the correct permissions!
Round 6 of 8!

Current permissions of "/challenge/pwn": ----w-rwx
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": ---r--r-x
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
* the world does have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod a=-,g=r,o=rx /challenge/pwn 
You set the correct permissions!
Round 7 of 8!

Current permissions of "/challenge/pwn": ---r--r-x
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": ---rw----
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod a=-,g=rw,o=- /challenge/pwn 
You set the correct permissions!
Round 8 of 8!

Current permissions of "/challenge/pwn": ---rw----
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": r-x-----x
* the user does have read permissions
- the user doesn't have write permissions
* the user does have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
* the world does have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod a=rx,
g=-,o=x /challenge/pwn 
You set the correct permissions!
You've solved all 8 rounds! I have changed the ownership
of the /flag file so that you can 'chmod' it. You won't be able to read
it until you make it readable with chmod!

Current permissions of "/flag": ---------
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permissions-setting-practice:~$ chmod a+r /flag 
hacker@permissions~permissions-setting-practice:~$ cat /flag 
pwn.college{cIyZu7i12wrwCa8gEbRDF3g_Bxw.QXzETO0wSOwAzNzEzW} 
```

### New Learnings
setting permissions of programs.

### References 
PWN College videos

## The SUID Bit
Set SUID bit to change permissions

### Solve
**Flag:** `pwn.college{kY7PHh9z60b-8YA5kPJ4qjl7fOu.QXzEjN0wSOwAzNzEzW}`

use chmod u+s to give owner permission as long as they have execute permission

```bash
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot 
hacker@permissions~the-suid-bit:~$ /challenge/getroot 
SUCCESS! You have set the suid bit on this program, and it is running as root! 
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag 
pwn.college{kY7PHh9z60b-8YA5kPJ4qjl7fOu.QXzEjN0wSOwAzNzEzW}
```

### New Learnings
setting SUID bit to give owner permission to users as long as they have execute permission.

### References 
PWN College videos