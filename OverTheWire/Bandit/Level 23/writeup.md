# Bandit Level 23 → Level 24

## 🧠 Objective
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.
---

## 🧰 Tools & Commands Used
- `cd`
- `nano`
- `ls`
- `chmod`
-  `ssh`

## 🕵️ Walkthrough

```bash
# Step 1: Connect via SSH
ssh bandit23@bandit.labs.overthewire.org -p 2220

#Step 2: Create directory to store shell needed to beat the level
mkdir /tmp/game1

#Step 3: Change the permissions of the directory to read and write so files can be copied to directory
chmod 777 /tmp/game1

#Step 3: Create the shell needed to beat the level in /var/spool/bandit24/foo
nano pass.sh

#!bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/game1/password

#Step 4: Go to the game1 directory and print password
cd /temp/game1
cat password
```
## 📌 Key Takeaways
- Learned how to write and implement and shell in the Linux


