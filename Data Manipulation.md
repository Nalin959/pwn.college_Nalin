# Data Manipulation

## Translating characters
Translate characters to change casing

### Solve
**Flag:** `pwn.college{MxofL9_0egrND6DrKou9TMisQ56.01MxEzNxwSOwAzNzEzW}`

use tr command to swap the characters with the required ones

```bash
hacker@data~translating-characters:~$ /challenge/run | tr qwertyuiopasdfghjklzxcvbnmQWERTYUIOPASDFGHJKLZXCVBNM QWERTYUIOPASD
FGHJKLZXCVBNMqwertyuiopasdfghjklzxcvbnm
yOUR CASE-SWAPPED FLAG:
pwn.college{MxofL9_0egrND6DrKou9TMisQ56.01MxEzNxwSOwAzNzEzW}
```

### New Learnings
use of tr command to swap characters.

### References 
none

## Deleting characters
Deleting characters from output

### Solve
**Flag:** `pwn.college{MxofL9_0egrND6DrKou9TMisQ56.01MxEzNxwSOwAzNzEzW}`

use tr with -d argument

```bash
hacker@data~deleting-characters:~$ /challenge/run | tr -d ^%
Your character-stuffed flag:
pwn.college{EIo-VH7z46nwaT892Sz40bvL7f4.0FNxEzNxwSOwAzNzEzW}
```

### New Learnings
use of tr -d command to delete characters from command output.

### References 
none

## Deleting newlines
Deleting newlines from output

### Solve
**Flag:** `pwn.college{UOnuvFmAjZECoF0h1Y5JEaf3O6-.0VNxEzNxwSOwAzNzEzW}`

use tr with -d argument to delete newline (\n)

```bash
hacker@data~deleting-newlines:~$ /challenge/run | tr -d  "\n"
Your line-split flag: pwn.college{UOnuvFmAjZECoF0h1Y5JEaf3O6-.0VNxEzNxwSOwAzNzEzW}
```

### New Learnings
use of \n to speciy newline in terminal.

### References 
none

## Extracting the first lines with head
Extract first lines with head

### Solve
**Flag:** `pwn.college{kEZr-j5DjOkS-HUbiHtK0niV_6k.0lNxEzNxwSOwAzNzEzW}`

pipe command to head with -n argument (n=7 here)

```bash
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -7 | /challenge/college 
Congratulations, you piped the right codes!
pwn.college{kEZr-j5DjOkS-HUbiHtK0niV_6k.0lNxEzNxwSOwAzNzEzW}
```

### New Learnings
using head to print first n lines.

### References 
none

## Extracting specific sections of text
Extract specific data from text

### Solve
**Flag:** `pwn.college{gct3wiMJiKzsOrBwMWNKoMRSTBw.01NxEzNxwSOwAzNzEzW}`

first run command to check output format, cut to show 2nd column with " " delimiter, then delete newline

```bash
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d ' ' -f 2 | tr -d '\n'
pwn.college{gct3wiMJiKzsOrBwMWNKoMRSTBw.01NxEzNxwSOwAzNzEzW}
```

### New Learnings
using cut and tr to extract specific data.

### References 
none

## Sorting Data
Sort data into a specific order

### Solve
**Flag:** `{oGETLoM8w69q6Dyf4ELjgo0j-aM.0FM0MDOxwSOwAzNzEzW}`

use sort -r to print the flag first as it prints alphabetically from Z to A

```bash
hacker@data~sorting-data:~$ sort /challenge/flags.txt -r
pwn.college{oGETLoM8w69q6Dyf4ELjgo0j-aM.0FM0MDOxwSOwAzNzEzW}
```

### New Learnings
sorting data using sort and its arguments.

### References 
none