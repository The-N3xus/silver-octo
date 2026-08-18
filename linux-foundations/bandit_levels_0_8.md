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