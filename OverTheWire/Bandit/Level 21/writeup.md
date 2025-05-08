# Bandit Level 21 → Level 22

## 🧠 Objective
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.
---

## 🧰 Tools & Commands Used
- `crontab`
- `cat`
- `cd`
- `ssh`

## 🕵️ Walkthrough

```bash
# Step 1: Connect via SSH
ssh bandit21@bandit.labs.overthewire.org -p 2220

#Step 2: Cd to /etc/cron.d
cd /etc/cron.d

#Step 3: Use cat to print on the specific command thats being executed by cron
cat cronjob_bandit22

# Step 4: Print the shell
cat /usr/bin/bash/cronjob_bandit22.sh

#Step 5: Use the directory in the shell to find the password
cat /tmp/t706....
```
## 📌 Key Takeaways
- Learned about cron