# File Globbing

## Matching with *
Using * in file matching

### Solve
**Flag:** `pwn.college{0tcKC8bqFqsxa8dFwfju1xV_stm.QXxIDO0wSOwAzNzEzW}`

use cd /ch* (*will look for the pattern)

```bash
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run 
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{0tcKC8bqFqsxa8dFwfju1xV_stm.QXxIDO0wSOwAzNzEzW}
```

### New Learnings
Using * (wildcard character) to find similar filenames with a given pattern.

### References 
none

## Matching with ?
Using ? in file matching

### Solve
**Flag:** `pwn.college{oRLzJkeU04AsunXCD-7LBEJ9YI5.QXyIDO0wSOwAzNzEzW}`

use cd /?ha??enge (? will only look for single character unlike *)

```bash
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run 
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{oRLzJkeU04AsunXCD-7LBEJ9YI5.QXyIDO0wSOwAzNzEzW}
hacker@globbing~matching-with-:/challenge$ 
```

### New Learnings
Using ? (single character wildcard) to find similar filenames with a given pattern. Here one ? will only account for one character unlike * where it can be anything after the pattern.

### References 
none

## Matching with []
Using [] in file matching

### Solve
**Flag:** `pwn.college{QJm5fO993awJR7N28jxNmbXOekk.QXzIDO0wSOwAzNzEzW}`

use cd /challenge/run file_[bash]. It will look for the characters b,a,s,h after file_

```bash
hacker@globbing~matching-with-:~$ cd /challenge/files/
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{QJm5fO993awJR7N28jxNmbXOekk.QXzIDO0wSOwAzNzEzW}
```

### New Learnings
Using [] for file matching. It works just like ? but we can specify the potential characters to be searched.

### References 
none

## Matching paths with []
Using [] in path matching

### Solve
**Flag:** `pwn.college{4WzgZirqENHx5id9uWxCiIgeQ5K.QX0IDO0wSOwAzNzEzW}`

/challenge/run /challenge/files/file_[bash] (use path instead of file name)

```bash
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{4WzgZirqENHx5id9uWxCiIgeQ5K.QX0IDO0wSOwAzNzEzW}
```

### New Learnings
Using [] for path matching. Same use as in file matching but path is searched here.

### References 
none

## Multiple globs
Using multiple globbing

### Solve
**Flag:** `pwn.college{4fcKm7VZGspXQSesQ8KQrQ2ga7Q.0lM3kjNxwSOwAzNzEzW}`

use /challenge/run *p* . * searches for words before and after p

```bash
hacker@globbing~multiple-globs:~$ cd /challenge/files/
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{4fcKm7VZGspXQSesQ8KQrQ2ga7Q.0lM3kjNxwSOwAzNzEzW}
```

### New Learnings
Using multiple globbing ie more than one search condition or pattern in a single word.

### References 
none

## Mixing globs
Using mixed globbing

### Solve
**Flag:** `pwn.college{kaF2iOgNI1Jgs0oSpuBDPaKpX6K.QX1IDO0wSOwAzNzEzW}`

/challenge/run [cep]*. * searches for words starting with c,e,p

```bash
hacker@globbing~mixing-globs:~$ cd /challenge/files/
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{kaF2iOgNI1Jgs0oSpuBDPaKpX6K.QX1IDO0wSOwAzNzEzW}
```

### New Learnings
Mixed use of file globbing. (everything from previous challenges)

### References 
none

## Exclusionary globs
Using exclusionary globbing

### Solve
**Flag:** `pwn.college{slty4Hswr123RhdF_FQ0sAwaaYs.QX2IDO0wSOwAzNzEzW}`

/challenge/run [^pwn]* (^ works like not operator)

```bash
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files/
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [^pwn]*
You got it! Here is your flag!
pwn.college{slty4Hswr123RhdF_FQ0sAwaaYs.QX2IDO0wSOwAzNzEzW}
```

### New Learnings
Using ^ for exclusionary globbing. ^ here gives result not matching the condition given.

### References 
none

## Tab completion
Using tab completion

### Solve
**Flag:** `pwn.college{slty4Hswr123RhdF_FQ0sAwaaYs.QX2IDO0wSOwAzNzEzW}`

use tab to complete the filename after typing pwn

```bash
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files/
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [^pwn]*
You got it! Here is your flag!
pwn.college{slty4Hswr123RhdF_FQ0sAwaaYs.QX2IDO0wSOwAzNzEzW}
```

### New Learnings
using tab key for filename completion.

### References 
none

## Multiple options for tab completion
Using tab completion with multiple options

### Solve
**Flag:** `pwn.college{IUZ3LEuvIb5EoSNOeXe2g3AGSzF.0lN0EzNxwSOwAzNzEzW}`

use tab to complete the filename then check the options available to get the flag

```bash
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwn
pwn                    pwncollege-flag
pwn-college            pwncollege-flamingo
pwn-the-planet         pwncollege-flyswatter
pwncollege-family      pwncollege-hacking
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-flag
pwn.college{IUZ3LEuvIb5EoSNOeXe2g3AGSzF.0lN0EzNxwSOwAzNzEzW}
```

### New Learnings
using tab key for filename completion with multiple options.

### References 
none

## Tab completion on commands
Using tab completion on commands

### Solve
**Flag:** `pwn.college{4Fo5Ag7J7ejQOgRRvf-mwOa_GaE.0VN0EzNxwSOwAzNzEzW}`

use tab to complete the command

```bash
hacker@globbing~tab-completion-on-commands:~$ pwncollege-20474 
Correct! Here is your flag:
pwn.college{4Fo5Ag7J7ejQOgRRvf-mwOa_GaE.0VN0EzNxwSOwAzNzEzW}
```

### New Learnings
using tab key to complete commands.

### References 
none