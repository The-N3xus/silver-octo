# OverTheWire Bandit: Levels 0 - 8

### Level 0 -> Level 1
**Objective:** Find the password hidden in the `readme` file.
**Commands Used:**
`cat readme`
**What I Learned:**
The `cat` command reads data from the file and outputs its contents directly to the terminal.
**Info for the next levels**
`Password:6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR`

---

### Level 1 -> Level 2
**Objective:** Find the password hidden in a file named `-`.
**Commands Used:**
`cat ./-`
**What I Learned:**
The `cat` command cannot operate properly when directories or file names are special characters or begin with them.
**Info for the next level**
`PK8fYLZg2hnHSz83plBL1iEPKdD3QToB`

---

### Level 2 -> Level 3
**Objective:**  Find the password hidden in a file with spaces in the name.
**Commands Used:**
`cat ./--spaces\ in\ the\ file\ name`
**What I Learned:**
For file names or directories with spaces in the names, you can either use quoation marks [""] for the command to read it as one or use the backward slash [\] to tell it to treat each slash as a space.
**Info for the next level**
`7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME`

---

### Level 3 -> Level 4
**Objective:** Find the password in a hidden directory
**Commands Used:**
` ls -a`
` cd ./inhere`
` ls -a`
` cat ./...Hiding-From-You`
` find ./inhere -type f -name ".*"
**What I learned:**
Some directories can have hidden files that won't show up if you only use the `ls` command but is you use the `ls -a` command then it reads all files hidden or not but that doesn't work then you can also try using the `find` command.
**Info for the next level**
`xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq`

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
**Info for the next level**
`6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG`

---
### Level 5 ->  Level 6
**Objective:** Find the hidden password with specific properties
**Commands Used:**
`cd ./inhere`
`find . -type f -size 1033c ! -executable`
`cat ./maybehere07/.file2`
**What I learned:**
I learned how to use the find command much better to suite the actions I am doing such as finding files that I don't know the name of or files I only know the properties of.
**Info for the next level**
`pXa26xhMWaC2SvDotA4r9EgZkulOeSBW`

---

### Level 6 ->  Level 7
**Objective:** Find the hidden password with specific properties but this time by ownership
**Commands Used:**
`cd ./inhere`
`find / -user bandit7 -group bandit6 -size 33c 2>/dev/null`
`cat /var/lib/dpkg/info/bandit7.password`
**What I learned:**
I learned how to use the find command to find files or directories by ownership as well as how to push 'permission denied' errors away when using a standard account without elevated priveleges and how to send error codes away so we don't see them in the terminal.
**Info for the next level**
`Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3`

---

### Level 7 -> Level 8
**Objective:** Find password in a text file next to the word millionth
**Commands Used:**
`ls`
`cat data.txt | grep "millionth"`
**What I learned:**
Today I learned how to use the grep commnand in searching for specific info in a file or directory as well as using the pipe command to feed results of one command into another
**Info for the next level**
`VR1ljMayciFxbnUokuQmJFw6QC9VKtub`

---

### Level 8 -> Level 9
**Objective:** Find the password hidden in a text file in a line of text that only occurs once in the file
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