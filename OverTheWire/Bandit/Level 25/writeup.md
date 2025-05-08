# Bandit Level 25 → Level 26

## 🧠 Objective
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not /bin/bash, but something else. Find out what it is, how it works and how to break out of it.
---

## 🧰 Tools & Commands Used
- `nc`
- `ssh`


## 🕵️ Walkthrough

```bash
# Step 1: Connect via SSH
ssh bandit25@bandit.labs.overthewire.org -p 2220

#Step 2: Use the sshkey to connect to bandit26, but also make screen small enough to show more

ssh  -i bandit26.sshey bandit26@bandit.labs.overthewire.org -p 2220

#Step 3: Press v to entire vim and then cat the password in the password's file

:r /etc/bandit_pass/bandit26