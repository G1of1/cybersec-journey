# Bandit Level 5 → Level 6

## 🧠 Objective
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

human-readable
1033 bytes in size
not executable
---

## 🧰 Tools & Commands Used
- `ssh`
- `ls`, `cat`, `find`
---

## 🕵️ Walkthrough

```bash
# Step 1: Connect via SSH
ssh bandit5@bandit.labs.overthewire.org -p 2220

# Step 2: Change directory to inhere
cd inhere

# Step 3: List the contents of the directory
ls

#Step 4: Find the correct file given the properties
find . -type f -size 1033c ! -executable

