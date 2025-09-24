# Comprehending commands

## cat: not the pet, but the command!
cat command

### Solve
**Flag:** `pwn.college{wgWjvRRbFGNhcoPTiJXesCpvV2W.QXxcTN0wSOwAzNzEzW}`

use cat flag

```bash
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag 
pwn.college{wgWjvRRbFGNhcoPTiJXesCpvV2W.QXxcTN0wSOwAzNzEzW}
```

### New Learnings
use of cat command

### References 
none


## catting absolote paths
cat command (absolute path)

### Solve
**Flag:** `pwn.college{0Z4qxx7Y0Ee7vs1FtmPs6UWOBID.QX5ETO0wSOwAzNzEzW}`

use cat /flag

```bash
hacker@commands~catting-absolute-paths:~$ cat /flag 
pwn.college{0Z4qxx7Y0Ee7vs1FtmPs6UWOBID.QX5ETO0wSOwAzNzEzW}
```

### New Learnings
use of cat command (absolute path)

### References 
none

## more cattin practice
cat command practice

### Solve
**Flag:** `pwn.college{0JvRyL3p-xt-bfVpWyKATHRV9br.QXwITO0wSOwAzNzEzW}`

navigate to required directory inside cat command

```bash
You cannot use the 'cd' command in this level, and must retrieve the flag by 
absolute path. Plus, I hid the flag in a different directory! You can find it 
in the file /usr/share/php7.4-mysql/flag. Go cat it out **without** cding into 
that directory!
hacker@commands~more-catting-practice:~$ cat /usr/share/php7.4-mysql/flag
pwn.college{0JvRyL3p-xt-bfVpWyKATHRV9br.QXwITO0wSOwAzNzEzW}
```

### New Learnings
use of cat command with file navigation

### References 
none

## grepping for a needle in a haystack
grep command

### Solve
**Flag:** `pwn.college{ELx2QcBjXsWrBUbkxwZ57PkjfG6.QX3EDO0wSOwAzNzEzW}`

use grep pwn.college /challenge/data.txt 

```bash
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt 
pwn.college{ELx2QcBjXsWrBUbkxwZ57PkjfG6.QX3EDO0wSOwAzNzEzW}
```

### New Learnings
use of grep command to find string in a file

### References 
none

## comparing files
diff command

### Solve
**Flag:** `pwn.college{glueL59M2i5O4NHwjBd5SIT-jCm.01MwMDOxwSOwAzNzEzW}`

use diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt

```bash
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
10a11
> pwn.college{glueL59M2i5O4NHwjBd5SIT-jCm.01MwMDOxwSOwAzNzEzW}
```

### New Learnings
use of diff command to compare to files

### References 
none

## listing files
ls command

### Solve
**Flag:** `pwn.college{MN-n-JEWJ2qtOfa7bGMSBRcpKve.QX4IDO0wSOwAzNzEzW}`

use ls /challenge and run the renamed file

```bash
hacker@commands~listing-files:~$ ls /challenge/
8035-renamed-run-11769  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/8035-renamed-run-11769 
Yahaha, you found me! Here is your flag:
pwn.college{MN-n-JEWJ2qtOfa7bGMSBRcpKve.QX4IDO0wSOwAzNzEzW}
```

### New Learnings
use of ls command to list contents of a directory

### References 
none

## touching files
touch command

### Solve
**Flag:** `pwn.college{EpO0u2Q77zM3zfvjI6EvU5q_F4y.QXwMDO0wSOwAzNzEzW}`

navigate to /tmp and create new files using touch

```bash
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ ls
bin  college  hsperfdata_root  pwn  tmp.TpSOPGOVKK
hacker@commands~touching-files:/tmp$ /challenge/run 
Success! Here is your flag:
pwn.college{EpO0u2Q77zM3zfvjI6EvU5q_F4y.QXwMDO0wSOwAzNzEzW}
hacker@commands~touching-files:/tmp$ 
```

### New Learnings
use of touch command to create files

### References 
none

## removing files
rm command

### Solve
**Flag:** `pwn.college{U4BaSVuY6WB0E31ZQrYhCrLLngW.QX2kDM1wSOwAzNzEzW}`

list files and then remove the required file

```bash
hacker@commands~removing-files:~$ ls
Desktop  Downloads  a  delete_me  not-the-flag  ourfile
hacker@commands~removing-files:~$ rm delete_me 
hacker@commands~removing-files:~$ ls
Desktop  Downloads  a  not-the-flag  ourfile
hacker@commands~removing-files:~$ /challenge/check 
Excellent removal. Here is your reward:
pwn.college{U4BaSVuY6WB0E31ZQrYhCrLLngW.QX2kDM1wSOwAzNzEzW}
```

### New Learnings
use of rm command to delete files

### References 
none

## moving files
mv command

### Solve
**Flag:** `pwn.college{EoRKk3DOJ8eax6nuoVvCU2jkg8i.0VOxEzNxwSOwAzNzEzW}`

use mv /flag /tmp/hack-the-planet

```bash
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check 
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{EoRKk3DOJ8eax6nuoVvCU2jkg8i.0VOxEzNxwSOwAzNzEzW}
```

### New Learnings
use of mv command to move files

### References 
none

## hidden files
ls -a command

### Solve
**Flag:** `pwn.college{4qIA5Lte_CEDSzkKnXO69VRnqn8.QXwUDO0wSOwAzNzEzW}`

use ls -a to find hidden flag file then use cat to read it

```bash
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.                      boot       lib     mnt   run   usr
..                     challenge  lib32   nix   sbin  var
.dockerenv             dev        lib64   opt   srv
.flag-317532131726349  etc        libx32  proc  sys
bin                    home       media   root  tmp
hacker@commands~hidden-files:/$ cat .flag-317532131726349 
pwn.college{4qIA5Lte_CEDSzkKnXO69VRnqn8.QXwUDO0wSOwAzNzEzW}
```

### New Learnings
use of -a argument in ls for showing hidden files

### References 
none

## An Epic Filesystem Quest
practice cd,ls,cat commands

### Solve
**Flag:** `pwn.college{E6khOWrSzlqfGlJzI1GbWmIczkx.QX5IDO0wSOwAzNzEzW}`

just follow the instructions

```bash
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
INSIGHT  challenge  flag  lib32   media  opt   run   sys  var
bin      dev        home  lib64   mnt    proc  sbin  tmp
boot     etc        lib   libx32  nix    root  srv   usr
hacker@commands~an-epic-filesystem-quest:/$ cat INSIGHT 
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/include/config/gcc

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/$ cd /opt/linux/linux-5.4/include/config/gcc
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/gcc$ ls -a
.  ..  .BRIEF  version.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/gcc$ cat .BRIEF 
Yahaha, you found me!
The next clue is in: /usr/share/doc/librest-0.7-0

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/gcc$ cd  /usr/share/doc/librest-0.7-0
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/librest-0.7-0$ ls -a
.  ..  .DISPATCH  changelog.Debian.gz  copyright
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/librest-0.7-0$ cat .DISPATCH 
Great sleuthing!
The next clue is in: /opt/linux/linux-5.4/drivers/gpu/drm/ast

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/librest-0.7-0$ cat  /opt/linux/linux-5.4/drivers/gpu/drm/ast/
Kconfig            ast_dram_tables.h  ast_mode.c
Makefile           ast_drv.c          ast_post.c
WHISPER-TRAPPED    ast_drv.h          ast_tables.h
ast_dp501.c        ast_main.c         ast_ttm.c
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/librest-0.7-0$ cat  /opt/linux/linux-5.4/drivers/gpu/drm/ast/WHISPER-TRAPPED 
Tubular find!
The next clue is in: /usr/lib/python3/dist-packages/twisted/internet/iocpreactor

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/librest-0.7-0$ cd /usr/lib/python3/dist-packages/twisted/internet/iocpreactor
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/twisted/internet/iocpreactor$ ls -a
.         __init__.py  const.py       reactor.py  udp.py
..        __pycache__  interfaces.py  setup.py
EVIDENCE  abstract.py  notes.txt      tcp.py
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/twisted/internet/iocpreactor$ cat EVIDENCE 
Great sleuthing!
The next clue is in: /usr/local/lib/python3.8/dist-packages/setuptools/_distutils/tests
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/twisted/internet/iocpreactor$ cd /usr/local/lib/python3.8/dist-packages/setuptools/_distutils/tests
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/setuptools/_distutils/tests$ ls -a
.                        test_dir_util.py
..                       test_dist.py
SECRET                   test_extension.py
__init__.py              test_file_util.py
__pycache__              test_filelist.py
compat                   test_install.py
support.py               test_install_data.py
test_archive_util.py     test_install_headers.py
test_bdist.py            test_install_lib.py
test_bdist_dumb.py       test_install_scripts.py
test_bdist_rpm.py        test_log.py
test_build.py            test_mingwccompiler.py
test_build_clib.py       test_modified.py
test_build_ext.py        test_msvccompiler.py
test_build_py.py         test_sdist.py
test_build_scripts.py    test_spawn.py
test_ccompiler.py        test_sysconfig.py
test_check.py            test_text_file.py
test_clean.py            test_unixccompiler.py
test_cmd.py              test_util.py
test_config_cmd.py       test_version.py
test_core.py             test_versionpredicate.py
test_cygwinccompiler.py  unix_compat.py
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/setuptools/_distutils/tests$ cat SECRET 
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/include/config/task/io

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/setuptools/_distutils/tests$ cd /opt/linux/linux-5.4/include/config/task/io
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/task/io$ ls -a
.  ..  DOSSIER  accounting.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/task/io$ cat DOSSIER 
Great sleuthing!
The next clue is in: /usr/share/doc/git/contrib/svn-fe
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/task/io$ cat  /usr/share/doc/git/contrib/svn-fe/
MESSAGE          svn-fe.c         svnrdump_sim.py
Makefile         svn-fe.txt       
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/task/io$ cat  /usr/share/doc/git/contrib/svn-fe/MESSAGE 
Great sleuthing!
The next clue is in: /opt/linux/linux-5.4/include/dt-bindings/mux

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/task/io$ cd /opt/linux/linux-5.4/include/dt-bindings/mux
bash: BLUEPRINT-TRAPPED: Permission denied
bash: BLUEPRINT-TRAPPED: Permission denied
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/dt-bindings/mux$ ls -a
bash: BLUEPRINT-TRAPPED: Permission denied
.  ..  BLUEPRINT-TRAPPED  mux.h
bash: BLUEPRINT-TRAPPED: Permission denied
bash: BLUEPRINT-TRAPPED: Permission denied
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/dt-bindings/mux$ cat BLUEPRINT-TRAPPED 
bash: BLUEPRINT-TRAPPED: Permission denied
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{E6khOWrSzlqfGlJzI1GbWmIczkx.QX5IDO0wSOwAzNzEzW}
bash: BLUEPRINT-TRAPPED: Permission denied
bash: BLUEPRINT-TRAPPED: Permission denied
```

### New Learnings
usecases of ls,cd,cat commands

### References 
SENSAI

## Symbolic Links
create a symbolic link to fool the system to giving you te flag

### Solve
**Flag:** `pwn.college{IKfYE5jxGUN-4lY8oc_Wtv_sUCL.QX5ETN1wSOwAzNzEzW}`

 use ln -s /flag  ~/not-the-flag and then /challenge/catflag

```bash
hacker@commands~linking-files:~$ ln -s /flag  ~/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag 
About to read out the /home/hacker/not-the-flag file!
pwn.college{IKfYE5jxGUN-4lY8oc_Wtv_sUCL.QX5ETN1wSOwAzNzEzW}
```

### New Learnings
use of symbolic links and ~

### References 
SENSAI,https://www.youtube.com/watch?v=m55AtwjBXpE&list=PL-ymxv0nOtqqRAz1x90vxNbhmSkeYxHVC