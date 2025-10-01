# Processes and Jobs

## Listing Processes
List processes using ps

### Solve
**Flag:** `pwn.college{cWp54e3jqqgLicMBXbJuaCOgVfJ.QX4MDO0wSOwAzNzEzW}`

use ps -aux or ps -ef to list all processes. use auxwwor efww is full path is not shown to disable truncation 

```bash
hacker@processes~listing-processes:~$ ps -aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  0.0   1056   640 ?        Ss   05:51   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace
root           7  0.0  0.0 231708  2560 ?        S    05:51   0:00 /run/dojo/bin/sleep 6h
root         132  0.0  0.0   4132  2560 ?        S    05:51   0:00 /challenge/28053-run-30481
root         135  0.0  0.0   2744  1600 ?        S    05:51   0:00 sleep 6h
hacker       146  0.0  0.0  37076 21760 ?        Sl   05:51   0:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bi
hacker       150  0.0  0.0 231940  4160 pts/0    Ss   05:51   0:00 /run/dojo/bin/bash --login
hacker       165  0.0  0.0 233600  3840 pts/0    R+   05:53   0:00 ps -aux
hacker@processes~listing-processes:~$ /challenge/28053-run-30481
Yahaha, you found me! Here is your flag:
pwn.college{cWp54e3jqqgLicMBXbJuaCOgVfJ.QX4MDO0wSOwAzNzEzW}
Now I will sleep for a while (so that you could find me with 'ps').
```

### New Learnings
listing process on terminal using ps.

### References 
none

## Killing Processes
Kill process using kill command

### Solve
**Flag:** `pwn.college{40MWrtcYr9JsVbrFimUiGABnuby.QXyQDO0wSOwAzNzEzW}`

use ps -aux or ps -ef to list all processes then kill the required process

```bash
hacker@processes~killing-processes:~$ ps -efww
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 06:04 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7       1  0 06:04 ?        00:00:00 /run/dojo/bin/sleep 6h
root         135       1  0 06:04 ?        00:00:00 su -c /challenge/.launcher hacker
hacker       136     135  0 06:04 ?        00:00:00 /challenge/dont_run
hacker       137     136  0 06:04 ?        00:00:00 sleep 6h
hacker       148       1  0 06:04 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --port 7681 --interface 0.0.0.0 --writable -t disableLeaveAlert true /run/dojo/bin/bash --login
hacker       152     148  0 06:05 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       165     152  0 06:08 pts/0    00:00:00 ps -efww
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge/run 
Great job! Here is your payment:
pwn.college{40MWrtcYr9JsVbrFimUiGABnuby.QXyQDO0wSOwAzNzEzW}
```

### New Learnings
killing process on terminal using kill.

### References 
none

## Interrupting Processes
Interrupt process using ctrl+c

### Solve
**Flag:** `pwn.college{svnIRUX_xhKEQKqemnquf5ThL2z.QXzQDO0wSOwAzNzEzW}`

use ctrl-c to close program running on terminal

```bash
hacker@processes~interrupting-processes:~$ /challenge/run 
I could give you the flag... but I won't, until this process exits. Remember, 
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{svnIRUX_xhKEQKqemnquf5ThL2z.QXzQDO0wSOwAzNzEzW}
```

### New Learnings
using ctrl+c to interrupt processes.

### References 
none

## Killing Misbehaving Processes
Kill misbehaving process using kill command

### Solve
**Flag:** `pwn.college{IHBZri3eXY9TgRxZJHsvmGWtV6M.0FNzMDOxwSOwAzNzEzW}`

kill decoy process and run /challenge/run in other terminal

```bash
hacker@processes~killing-misbehaving-processes:~$ ps -efww
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 07:49 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7       1  0 07:49 ?        00:00:00 /run/dojo/bin/sleep 6h
root         137       1  0 07:49 ?        00:00:00 /bin/bash /challenge/.init
root         138       1  0 07:49 ?        00:00:00 /bin/bash /challenge/.init
root         139       1  0 07:49 ?        00:00:00 su -c exec /challenge/decoy > /tmp/flag_fifo hacker
root         140     137  0 07:49 ?        00:00:00 sleep 6h
root         141     138  0 07:49 ?        00:00:00 sleep 6h
hacker       142     139  0 07:49 ?        00:00:00 /usr/bin/python /challenge/decoy
hacker       153       1  4 07:49 ?        00:00:00 /nix/store/a1kxazxkgw7mjbjgisvah95p1r3n5ykl-nodejs-22.16.0/bin/node /nix/store/5hs5m65ajn7i3s6k20gzks9s7g5avn3w-code-server/libexec/code-server/out/node/entry.js --auth=none --bind-addr=0.0.0.0:8080 --trusted-origins=* --disable-telemetry --extensions-dir=/nix/store/yq56055z34blyalmlby87c7g8c361r1g-code-service/share/code/extensions --config=/dev/null
hacker       176     153 22 07:49 ?        00:00:03 /nix/store/a1kxazxkgw7mjbjgisvah95p1r3n5ykl-nodejs-22.16.0/bin/node /nix/store/5hs5m65ajn7i3s6k20gzks9s7g5avn3w-code-server/libexec/code-server/out/node/entry
hacker       215     176 14 07:49 ?        00:00:01 /nix/store/a1kxazxkgw7mjbjgisvah95p1r3n5ykl-nodejs-22.16.0/bin/node --dns-result-order=ipv4first /nix/store/5hs5m65ajn7i3s6k20gzks9s7g5avn3w-code-server/libexec/code-server/lib/vscode/out/bootstrap-fork --type=extensionHost --transformURIs --useHostProxy=false
hacker       233     176  4 07:49 ?        00:00:00 /nix/store/a1kxazxkgw7mjbjgisvah95p1r3n5ykl-nodejs-22.16.0/bin/node /nix/store/5hs5m65ajn7i3s6k20gzks9s7g5avn3w-code-server/libexec/code-server/lib/vscode/out/bootstrap-fork --type=ptyHost --logsPath /home/hacker/.local/share/code-server/logs/20251001T074919
hacker       296     233  0 07:49 pts/1    00:00:00 /run/dojo/bin/bash --init-file /nix/store/5hs5m65ajn7i3s6k20gzks9s7g5avn3w-code-server/libexec/code-server/lib/vscode/out/vs/workbench/contrib/terminal/browser/media/shellIntegration-bash.sh
hacker       358     296  0 07:49 pts/1    00:00:00 ps -efww
hacker@processes~killing-misbehaving-processes:~$ kill 142
hacker@processes~killing-misbehaving-processes:~$ /challenge/run 
Sending the flag to /tmp/flag_fifo!
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo 
pwn.college{IHBZri3eXY9TgRxZJHsvmGWtV6M.0FNzMDOxwSOwAzNzEzW}
```

### New Learnings
killing misbehaving process on terminal using kill.

### References 
SENSAI

## Suspending Processes
Suspending process using ctrl+z

### Solve
**Flag:** `pwn.college{UtaJg2Uz8iVIrM4ZQ6HlJQJzWl1.QX1QDO0wSOwAzNzEzW}`

run command, suspend using ctrl+z and run again

```bash
hacker@processes~suspending-processes:~$ /challenge/run 
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         146     136  0 08:02 pts/0    00:00:00 bash /chal
root         148     146  0 08:02 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can 
background me with Ctrl-Z or, if you're not ready to do that for whatever 
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run 
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         146     136  0 08:02 pts/0    00:00:00 bash /chal
root         153     136  0 08:02 pts/0    00:00:00 bash /chal
root         155     153  0 08:02 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{UtaJg2Uz8iVIrM4ZQ6HlJQJzWl1.QX1QDO0wSOwAzNzEzW}
```

### New Learnings
suspending processes using ctrl+z.

### References 
none

## Resuming Processes
Resuming process using fg

### Solve
**Flag:** `pwn.college{gw2VdssykL_TRcpSUpXmki02Ck2.QX2QDO0wSOwAzNzEzW}`

run command suspend using ctrl+z and resume using fg

```bash
hacker@processes~resuming-processes:~$ /challenge/run 
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with 
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{gw2VdssykL_TRcpSUpXmki02Ck2.QX2QDO0wSOwAzNzEzW}
Don't forget to press Enter to quit me!

Goodbye!
```

### New Learnings
resuming processes using fg in foreground of terminal.

### References 
none

## Backgrounding Processes
Backgrounding process using bg

### Solve
**Flag:** `pwn.college{Yb_-wKLXFdwD5n2f3VT3DCzS3kt.QX3QDO0wSOwAzNzEzW}`

run command suspend using ctrl+z and resume using bg

```bash
hacker@processes~backgrounding-processes:~$ /challenge/run 
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         147 S+   bash /challenge/run
root         149 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the 
background, and then launch a new version of me! You can background me with 
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to 
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~backgrounding-processes:~$ 


Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out.

hacker@processes~backgrounding-processes:~$ /challenge/run 
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         147 S    bash /challenge/run
root         157 S    sleep 6h
root         158 S+   bash /challenge/run
root         160 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{Yb_-wKLXFdwD5n2f3VT3DCzS3kt.QX3QDO0wSOwAzNzEzW}
hacker@processes~backgrounding-processes:~$ 
```

### New Learnings
resuming processes using bg in background of terminal.

### References 
none

## Foregrounding Processes
Foreground backgrounded process using fg

### Solve
**Flag:** `pwn.college{4_-4XjjgbTMAuN7F8ZXTNyrclfL.QX4QDO0wSOwAzNzEzW}`

run command suspend using ctrl+z and resume in background using bg, the foreground it using fg

```bash
hacker@processes~foregrounding-processes:~$ /challenge/run 
To pass this level, you need to suspend me, resume the suspended process in the 
background, and *then* foreground it without re-suspending it! You can 
background me with Ctrl-Z (and resume me in the background with 'bg') or, if 
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~foregrounding-processes:~$ 


Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out. After that, resume me into the foreground with 'fg'; 
I'll wait.

hacker@processes~foregrounding-processes:~$ fg
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{4_-4XjjgbTMAuN7F8ZXTNyrclfL.QX4QDO0wSOwAzNzEzW}
```

### New Learnings
foreground backgrounded process using bg then fg.

### References 
none

## Starting Backgrounded Processes
Starting Backgrounded Processes using &

### Solve
**Flag:** `pwn.college{4_-4XjjgbTMAuN7F8ZXTNyrclfL.QX4QDO0wSOwAzNzEzW}`

use & symbol to run command in backgroung from the start

```bash
hacker@processes~starting-backgrounded-processes:~$ /challenge/run 
You've started me in the foreground! You must start me in the background (by 
appending '&' to the command) to get the flag!
hacker@processes~starting-backgrounded-processes:~$ /challenge/run&
[1] 163
hacker@processes~starting-backgrounded-processes:~$ 


Yay, you started me in the background! Because of that, this text will probably 
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{EFdz9q2CjNzuq3BkVHmXk3WxInG.QX5QDO0wSOwAzNzEzW}

[1]+  Done                    /challenge/run
```

### New Learnings
starting processes in background using &.

### References 
none

## Processing Exit Codes
Retrieve exit code

### Solve
**Flag:** `pwn.college{gLzy7w9n1lwNzeWPdRRgsi3ZIdb.QX5YDO1wSOwAzNzEzW}`

use $? to get exit code after running command

```bash
hacker@processes~process-exit-codes:~$ /challenge/get-code 
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
118
hacker@processes~process-exit-codes:~$ /challenge/submit-code 118
CORRECT! Here is your flag:
pwn.college{gLzy7w9n1lwNzeWPdRRgsi3ZIdb.QX5YDO1wSOwAzNzEzW}
```

### New Learnings
working with exit codes using $?.

### References 
none