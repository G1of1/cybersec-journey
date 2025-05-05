# Bandit Level 19 → Level 20

## 🧠 Objective
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.
---

## 🧰 Tools & Commands Used
- `ssh`

## 🕵️ Walkthrough

```bash
# Step 1: Connect via SSH
ssh bandit15@bandit.labs.overthewire.org -p 2220

# Step 2: List all the directory or files in the machine
ls 
ls -la

#Step 3: Run ./bandit20-do to see what it does
./bandit20-do

#Step 4: Run with the cat commands to display the password in the directory given above
./bandit20-do cat /etc/bandit_pass/bandit20


