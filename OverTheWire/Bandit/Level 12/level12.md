# Bandit Level 12 → Level 13

## 🧠 Objective
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 position
---

## 🧰 Tools & Commands Used
- `ssh`
-  `cat`, `file`, `tar`, `gzip`, `bzip2`, `mkdir`, `xxd`, `mv`

## 🕵️ Walkthrough

```bash
# Step 1: Connect via SSH
ssh bandit12@bandit.labs.overthewire.org -p 2220

#Step 1: Change directory into /tmp and make another directory
cd /tmp
mkdir lebron

# Step 2: Use xxd to create a hexdump file of the data.txt
cat data.txt | xxd -r > hexdump

#Step 3: Use mv to change hexdump into a gz file
mv hexdump hexdump.gz

#Step 4: Compress the file
gzip -d hexdump.gz

#Step 5: Use mv to change hexdum to a bz2 file
mv hexdump hexdump.bz2

#Step 6: Compress the file
bzip2 -d hexdump.bz2

#Step 7: Change file to gz file
mv hexdump hexdump.gz

#Step 8: Compress file
gzip -d hexdump.gz

#Step 9: Use tar to extract the file
tar -xvf hexdump

#Step 10: Use file to determine the type of file, repeat until file is ASCII
```
## 📌 Key Takeaways
- Learned about gzip, tar, mv and other commands.
- Learned about hexdumps
- Learned about compression tools in Linux

