# Bandit Level 11 → Level 12

### Level Goal
The password for the next level is stored in the file `data.txt`, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

---

### Solution

```bash
# tr = translate, 'A-Za-z' all lower and upper case letters, 
# 'N-ZA-Mn-za-m' alphabet rotated 13 times 
tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt # here it is
exit
ssh -p 2220 bandit12@bandit.labs.overthewire.org
7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```
