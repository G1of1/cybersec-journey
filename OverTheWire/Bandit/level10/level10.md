# Bandit Level 10 → Level 11

## 🧠 Objective
The password for the next level is stored in the file data.txt, which contains base64 encoded data
---

## 🧰 Tools & Commands Used
- `ssh`
-  `cat`, `base64`
---

## 🕵️ Walkthrough

```bash
# Step 1: Connect via SSH
ssh bandit10@bandit.labs.overthewire.org -p 2220

# Step 2: Use base64 to see the data
base64 data.txt

#Step 3: Use -d to view the string
cat data.txt | base64 -d

