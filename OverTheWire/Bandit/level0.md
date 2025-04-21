# Bandit Level X → Level X+1

## 🧠 Objective
> Description of the goal for this level as stated on the Bandit site.

_Example:_  
"The password for the next level is stored in a file called `readme` located in the home directory."

---

## 🧰 Tools & Commands Used
- `ssh`
- `ls`, `cat`, `file`, `find`
- `grep`, `du`, `sort`, `awk`, `xargs`
- Redirection: `>`, `<`, `>>`, `|`
- `base64`, `xxd`, `tar`, `gzip`, `bzip2`, etc.

---

## 🕵️ Walkthrough

```bash
# Step 1: Connect via SSH
ssh banditX@bandit.labs.overthewire.org -p 2220

# Step 2: Discover the file
ls -la

# Step 3: Read contents of the file
cat readme