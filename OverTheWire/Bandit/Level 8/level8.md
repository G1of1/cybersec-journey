# Bandit Level 8 → Level 9

## 🧠 Objective
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

## 🧰 Tools & Commands Used
- `ssh`
- `cat`,
---

## 🕵️ Walkthrough

```bash
# Step 1: Connect via SSH
ssh bandit8@bandit.labs.overthewire.org -p 2220

# Step 2: Use cat to find with sort, unqiue and count to find the password
cat data.txt | sort | uniq -c
```

## 📌 Key Takeaways
- Learned the sort command and some of the its unique use cases such as this level.