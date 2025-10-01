# Untangling Users

## Becoming root with su
Become root user

### Solve
**Flag:** `pwn.college{Y3eTe8fYhPJ7fjSSxDVWZN-HaFw.QX1UDN1wSOwAzNzEzW}`

enter password and read flag

```bash
hacker@users~becoming-root-with-su:~$ su
Password: 
root@users~becoming-root-with-su:/home/hacker# cat /flag 
pwn.college{Y3eTe8fYhPJ7fjSSxDVWZN-HaFw.QX1UDN1wSOwAzNzEzW}
```

### New Learnings
Becoming a root user (administrator) of a system.

### References 
none

## Other users with su
Become any other user

### Solve
**Flag:** `pwn.college{swiZFhpBAPZ9bDoumo2KRcLrAyV.QX2UDN1wSOwAzNzEzW}`

use su zardus to sign in and enter password

```bash
hacker@users~other-users-with-su:~$ su zardus
Password: 
zardus@users~other-users-with-su:/home/hacker$ /challenge/run 
Congratulations, you have become Zardus! Here is your flag:
pwn.college{swiZFhpBAPZ9bDoumo2KRcLrAyV.QX2UDN1wSOwAzNzEzW}
```

### New Learnings
Becoming any other user of a system.

### References 
none


## Cracking passwords
Crack passwords using john the ripper

### Solve
**Flag:** `pwn.college{Um-A02lZ15TM2tzMkOyRGQtL6Za.QX3UDN1wSOwAzNzEzW}`

use john command to crack all hashed passwords

```bash
n:*:20182:0:99999:7:::
bin:*:20182:0:99999:7:::
sys:*:20182:0:99999:7:::
sync:*:20182:0:99999:7:::
games:*:20182:0:99999:7:::
man:*:20182:0:99999:7:::
lp:*:20182:0:99999:7:::
mail:*:20182:0:99999:7:::
news:*:20182:0:99999:7:::
uucp:*:20182:0:99999:7:::
proxy:*:20182:0:99999:7:::
www-data:*:20182:0:99999:7:::
backup:*:20182:0:99999:7:::
list:*:20182:0:99999:7:::
irc:*:20182:0:99999:7:::
gnats:*:20182:0:99999:7:::
nobody:*:20182:0:99999:7:::
_apt:*:20182:0:99999:7:::
systemd-timesync:*:20357:0:99999:7:::
systemd-network:*:20357:0:99999:7:::
systemd-resolve:*:20357:0:99999:7:::
mysql:!:20357:0:99999:7:::
messagebus:*:20357:0:99999:7:::
sshd:*:20357:0:99999:7:::
hacker::20357:0:99999:7:::
zardus:$6$tCA5B.Kd8StQJl3S$xVsFbLyDwUOgKC988T2KhYn/jIrVSR2NtFnVus/vceIbTVl31LuRfKaCjiQWyJAojmJhAOcq45G6eMgKeBYDo/:20362:0:99999:7:::
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak 
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:20 100% 2/3 0.04784g/s 278.6p/s 278.6c/s 278.6C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak --show
hacker:NO PASSWORD:20357:0:99999:7:::
zardus:aardvark:20362:0:99999:7:::

2 password hashes cracked, 0 left
hacker@users~cracking-passwords:~$ su zardus
Password: 
zardus@users~cracking-passwords:/home/hacker$ /challenge/run 
Congratulations, you have become Zardus! Here is your flag:
pwn.college{Um-A02lZ15TM2tzMkOyRGQtL6Za.QX3UDN1wSOwAzNzEzW}
```

### New Learnings
cracking passwords using john the ripper program.

### References 
none

## Using sudo
Use sudo to elevate priviledges

### Solve
**Flag:** `pwn.college{gYrG28PkDNS48yiWcIeDFRqbU08.QX4UDN1wSOwAzNzEzW}`

use sudo

```bash
hacker@users~using-sudo:~$ sudo cat /flag 
pwn.college{gYrG28PkDNS48yiWcIeDFRqbU08.QX4UDN1wSOwAzNzEzW}
```

### New Learnings
using sudo to elevate priviledges.

### References 
none