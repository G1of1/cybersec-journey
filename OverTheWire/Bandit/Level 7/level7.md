# Bandit Level 7 → Level 8

## 🧠 Objective
The password for the next level is stored in the file data.txt next to the word millionth
---

## 🧰 Tools & Commands Used
- `ssh`
- `ls`, `cat`, `find`
---

## 🕵️ Walkthrough

```bash
# Step 1: Connect via SSH
ssh bandit7@bandit.labs.overthewire.org -p 2220

# Step 2: Use grep to find the millionth to see the words near millionth
grep "millionth" data.txt
```
## 📌 Key Takeaways
- Learned to use the command grep and figure out some of its use cases