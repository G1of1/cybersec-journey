# Bandit Level 11 → Level 12

## 🧠 Objective
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 position
---

## 🧰 Tools & Commands Used
- `ssh`
-  `cat`, `base64`
- rot13 decoder

## 🕵️ Walkthrough

```bash
# Step 1: Connect via SSH
ssh bandit11@bandit.labs.overthewire.org -p 2220

# Step 2: Print out the contents of the data.txt file
cat data.txt

#Step 3: Use rot13 decoder to decypher the password