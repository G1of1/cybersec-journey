# Bandit Level 6 → Level 7

## 🧠 Objective
The password for the next level is stored somewhere on the server and has all of the following properties:

owned by user bandit7
owned by group bandit6
33 bytes in size
---

## 🧰 Tools & Commands Used
- `ssh`
- `find`
---

## 🕵️ Walkthrough

```bash
# Step 1: Connect via SSH
ssh bandit6@bandit.labs.overthewire.org -p 2220

# Step 2: Use find with the given properties to find the password
find / -type f -user bandit7 -group bandit6 -size 33c
