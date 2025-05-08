# Bandit Level 22 → Level 23

## 🧠 Objective
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.
---

## 🧰 Tools & Commands Used
-  `cat`
-  `cd`
-  `ls`
-  `ssh`

## 🕵️ Walkthrough

```bash
# Step 1: Connect via SSH
ssh bandit22@bandit.labs.overthewire.org -p 2220

#Step 2: cd to /etc/cron.d
cd /etc/cron.d

# Step 3: Open the cronjob for bandit23
cat cronjob_bandit23

#Step 4: Print the shell
cat /usr/bin/cronjob_bandit23.sh


#Step 3: Define variables for the shell
nyame=bandit23
echo I am user bandit23 | md5sum 

# Step 4: Copy the target and cd to target file to find password
cat /tmp/<target>
```
## 📌 Key Takeaways
- Learned about how to interact with shells