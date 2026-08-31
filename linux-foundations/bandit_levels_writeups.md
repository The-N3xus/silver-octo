# OverTheWire Bandit: Levels 0 - 8

### Level 0 -> Level 1
**Objective:** Find the password hidden in the `readme` file.

**Commands Used:**
`cat readme`

**What I Learned:**
The `cat` command reads data from the file and outputs its contents directly to the terminal.

---

### Level 1 -> Level 2
**Objective:** Find the password hidden in a file named `-`.

**Commands Used:**
`cat ./-`

**What I Learned:**
The `cat` command cannot operate properly when directories or file names are special characters or begin with them.

---

### Level 2 -> Level 3
**Objective:**  Find the password hidden in a file with spaces in the name.

**Commands Used:**
`cat ./--spaces\ in\ the\ file\ name`

**What I Learned:**
For file names or directories with spaces in the names, you can either use quoation marks [""] for the command to read it as one or use the backward slash [\] to tell it to treat each slash as a space.

---

### Level 3 -> Level 4
**Objective:** Find the password in a hidden directory.

**Commands Used:**
` ls -a`
` cd ./inhere`
` ls -a`
` cat ./...Hiding-From-You`
` find ./inhere -type f -name ".*"

**What I learned:**
Some directories can have hidden files that won't show up if you only use the `ls` command but is you use the `ls -a` command then it reads all files hidden or not but that doesn't work then you can also try using the `find` command.

---

### Level 4 -> Level 5
**Objective:** Find the hidden password in a hidden directory but from the only Human readable file in a bunch of dummy files.

**Commands Used:**
`ls -a`
`cd ./inhere`
`ls -a`
`cat -- -file07`

**What I learned:**
Finding the hidden files was not hard this time but I did have to cycle through the files until I landed on the right file. 
Or you can use "find -type f -exec sh -c 'file --mime-type "$1" | grep -q "text/"' _ {} \; -print" though it worked I can't really explain how yet.

---
### Level 5 ->  Level 6
**Objective:** Find the hidden password with specific properties.

**Commands Used:**
`cd ./inhere`
`find . -type f -size 1033c ! -executable`
`cat ./maybehere07/.file2`

**What I learned:**
I learned how to use the find command much better to suite the actions I am doing such as finding files that I don't know the name of or files I only know the properties of.

---

### Level 6 ->  Level 7
**Objective:** Find the hidden password with specific properties but this time by ownership.

**Commands Used:**
`cd ./inhere`
`find / -user bandit7 -group bandit6 -size 33c 2>/dev/null`
`cat /var/lib/dpkg/info/bandit7.password`

**What I learned:**
I learned how to use the find command to find files or directories by ownership as well as how to push 'permission denied' errors away when using a standard account without elevated priveleges and how to send error codes away so we don't see them in the terminal.

---

### Level 7 -> Level 8
**Objective:** Find password in a text file next to the word millionth.

**Commands Used:**
`ls`
`cat data.txt | grep "millionth"`

**What I learned:**
Today I learned how to use the grep commnand in searching for specific info in a file or directory as well as using the pipe command to feed results of one command into another.

---

### Level 8 -> Level 9
**Objective:** Find the password hidden in a text file in a line of text that only occurs once in the file

**Commands Used:**
`sort data.txt | uniq -u`

**What I learned:**
Today I learned that I can use a command called `uniq` to pick out duplicate lines in a text file but it only does that for the lines adjacent to each other not the whole file, so then you need to use it hand in hand with the `sort` command to present the information in alphabetical order in order to for the `uniq` command to run as intended.

**Info for the next level**
`EjmOSvuAu7sGAHqHVcBDPirRe9T03kxl`

---

### Level 9 -> Level 10
**Objective:** Find the password hidden in the data.txt file and it is hidden as one of the few human readable strings preceded by several "=" characters.

**Commands Used:**
`ls`
`strings data.txt | grep "="`

**What I learned:**
In cases where a file is littered with non human readable noise you can use the `strings` command to filter through all that and just give you what is readable by humans and then I piped that output to the `grep` command to give me only the characters preceeded by several '=' as instructed.

**Info for the next level**
`B0s2khmbT9u0geKuOoVGW3JZKhndE3BG`

---

### Level 10 -> Level 11
**Objective:**  Find the password in a file that is using base64 encoding.

**Commands Used:**
`ls`
`echo "VGhlIHBhc3N3b3JkIGlzIHBZZk9ZNkh3VXNEajVyTDlVdnloVTdNQ212OHZONVJvCg==" | base64 -d`

**What I learned:**
When dealing with encrypted info or files that use a different encodinng you need to de-encode them first to be able to use them. That is where the `base64 -d` command came in handy to de-encode the file first and give me the inof I needed.

**Info for the next level**
`pYfOY6HwUsDj5rL9UvyhU7MCmv8vN5Ro`

---

### Level 11 -> Level 12
**Objective:** Find the password in a data.txt file where all the lowercase [a-z] and uppercase [A-Z] characters have been rotated 13 times.

**Commands Used:**
`ls`
`cat data.txt | tr 'a-zA-Z' 'n-za-mN-ZA-M'` or `tr 'a-zA-Z' 'n-za-mN-ZA-M' < data.txt`

**What I learned:**
The passowrd was encrypted using the ROT13 method that rotates characters of the alphabet every 13th letter. Inorder to solve this puzzle I needed to use the `tr` command that sorts the data from the original output 'Set1' to a new 'Set2" using the criteria you provide.

**Info for the next level**
`GROozWPO8QyN0mGrjUkID0WCYkZiQxrN`

---

### Level 12 -> Level 13
**Objective:** 
**Commands Used:**
**What I learned:**
**Info for the next level**

---

### Level 7 -> Level 8
**Objective:** 
**Commands Used:**
**What I learned:**
**Info for the next level**

---

### Level 7 -> Level 8
**Objective:** 
**Commands Used:**
**What I learned:**
**Info for the next level**

---

### Level 7 -> Level 8
**Objective:** 
**Commands Used:**
**What I learned:**
**Info for the next level**

---

### Level 7 -> Level 8
**Objective:** 
**Commands Used:**
**What I learned:**
**Info for the next level**

---

### Level 7 -> Level 8
**Objective:** 
**Commands Used:**
**What I learned:**
**Info for the next level**

---

### Level 7 -> Level 8
**Objective:** 
**Commands Used:**
**What I learned:**
**Info for the next level**

---