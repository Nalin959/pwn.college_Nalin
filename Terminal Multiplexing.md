# Terminal Multiplexing

## Launching Screen
Launch screen in terminal

### Solve
**Flag:** `pwn.college{helloworld}`

use screen command

```bash
Congratulations! You're inside a screen session!
Here's your flag:
pwn.college{IXI4t5t8iJTUV6vsUMSpVdWCG8_.0VN4IDOxwSOwAzNzEzW}
```

### New Learnings
screen launcher a virtual terminal inside the terminal, it is like multiple browser tabs.

### References 
none

## Detaching and Attaching
Launch screen in terminal

### Solve
**Flag:** `pwn.college{wAVP3trcKBF2lkQ-vT0dEjQEEy0.0lN4IDOxwSOwAzNzEzW}`

use screen command, exit using ctrl+d or exit and reattach using screen -r

```bash
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen
[detached from 168.pts-0.terminal-multiplexing~detaching-and-attaching]
hacker@terminal-multiplexing~detaching-and-attaching:~$ /challenge/run 
Found detached screen session: 157.pts-0.terminal-multiplexing~detaching-and-attaching
Sending flag to your screen session...

Flag sent! Now reattach to your screen session with:

  screen -r

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching:~$ echo Yes! Flag is: pwn.college{wAVP3trcKBF2lkQ-vT0dEjQEEy0.0lN4IDOxwSOwAzNzEzW}
Yes! Flag is: pwn.college{wAVP3trcKBF2lkQ-vT0dEjQEEy0.0lN4IDOxwSOwAzNzEzW}
```

### New Learnings
attaching and detaching screen(screen -r, ctrl+a then press d).

### References 
none

## Finding Sessions
Finding sessions in terminal

### Solve
**Flag:** `pwn.college{UXrc-_p7AnQ1onS_8aXOaCo3-mT.01N4IDOxwSOwAzNzEzW}`

use screen -ls to find running sessions then check one by one for flag using screen -r "session"

```bash
hacker@terminal-multiplexing~finding-sessions:~$ screen -ls
There are screens on:
        215.pts-0.terminal-multiplexing~launching-screen        (Remote or dead)
        157.pts-0.terminal-multiplexing~detaching-and-attaching (Remote or dead)
        168.pts-0.terminal-multiplexing~detaching-and-attaching (Remote or dead)
        193.pts-0.terminal-multiplexing~detaching-and-attaching (Remote or dead)
        147.pts-0.terminal-multiplexing~detaching-and-attaching (Remote or dead)
        145.session_208bebd40a65606c    (Detached)
        148.session_ff53ee1103615863    (Detached)
        151.session_9c35fc54781ac905    (Detached)
8 Sockets in /home/hacker/.screen.
hacker@terminal-multiplexing~finding-sessions:~$ screen -r 145
[screen is terminating]
hacker@terminal-multiplexing~finding-sessions:~$  echo 'Congratulations! You found the right session!'
Congratulations! You found the right session!
hacker@terminal-multiplexing~finding-sessions:~$  echo pwn.college{UXrc-_p7AnQ1onS_8aXOaCo3-mT.01N4IDOxwSOwAzNzEzW}
pwn.college{UXrc-_p7AnQ1onS_8aXOaCo3-mT.01N4IDOxwSOwAzNzEzW}
```

### New Learnings
Working with multiple screen sessions.

### References 
none

## Switching Windows
Switching screens in terminal

### Solve
**Flag:** `pwn.college{8lZ9Amq6MGC-sP_0P8T30zbNRl1.0FO4IDOxwSOwAzNzEzW}`

use screen -r then navigate using ctrl+a

```bash
hacker@terminal-multiplexing~switching-windows:~$ screen -r
hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{8lZ9Amq6MGC-sP_0P8T30zbNRl1.0FO4IDOxwSOwAzNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{8lZ9Amq6MGC-sP_0P8T30zbNRl1.0FO4IDOxwSOwAzNzEzW}
hacker@terminal-multiplexing~switching-windows:~$
```

### New Learnings
switching screens in terminal using ctrl+a.

### References 
none

## Detaching and Attaching (tmux)
Detaching and attaching using tmux

### Solve
**Flag:** `pwn.college{wvdsWp3PrM7T8T1lM1oFfzSZe3M.0VO4IDOxwSOwAzNzEzW}`

use tmux, tmux ls, tmux a instead of screen and use ctrl+b instead of ctrl+a

```bash
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux
[detached (from session 0)]
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ /challenge/run 
Found detached tmux session: 0
Sending flag to your tmux session...

Flag sent! Now reattach to your tmux session with:
  tmux attach

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux a
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$  echo Congratulations, here is your flag: pwn.college{wvdsWp3PrM7T8T1lM1oFfzSZe3M.0VO4IDOxwSOwAzNzEzW}
Congratulations, here is your flag: pwn.college{wvdsWp3PrM7T8T1lM1oFfzSZe3M.0VO4IDOxwSOwAzNzEzW}
```

### New Learnings
attaching and detaching using tmux instead of screen

### References 
none

## Switching Windows (tmux)
Switching Windows using tmux

### Solve
**Flag:** `pwn.college{U_XqL8njT4fPS551zs6M_AAXaQc.0FM5IDOxwSOwAzNzEzW}`

use tmux, ctrl+b to navigate

```bash
 cat <<MSG
Welcome to the tmux window switching challenge!
You are currently in window 1.
The flag is hidden in window 0.
Use Ctrl-B 0 to switch to window 0!
MSG
hacker@terminal-multiplexing~switching-windows-tmux:~$  cat <<MSG
> Welcome to the tmux window switching challenge!
> You are currently in window 1.
> The flag is hidden in window 0.
> Use Ctrl-B 0 to switch to window 0!
> MSG
Welcome to the tmux window switching challenge!
You are currently in window 1.
The flag is hidden in window 0.
Use Ctrl-B 0 to switch to window 0!
hacker@terminal-multiplexing~switching-windows-tmux:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{U_XqL8njT4fPS551zs6M_AAXaQc.0FM5IDOxwSOwAzNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{U_XqL8njT4fPS551zs6M_AAXaQc.0FM5IDOxwSOwAzNzEzW}
hacker@terminal-multiplexing~switching-windows-tmux:~$ 
```

### New Learnings
Switching screens using tmux instead of screen

### References 
none