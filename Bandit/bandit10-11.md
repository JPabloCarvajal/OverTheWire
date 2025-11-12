# Bandit Level 10 → Level 11

### Level Goal
The password for the next level is stored in the file `data.txt`, which contains base64 encoded data

---

### Solution

```bash
ls -la
# The -d flag tells the command to decode the input, returning the original string.
cat data.txt | base64 -d # here it is
exit
ssh -p 2220 bandit11@bandit.labs.overthewire.org
dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```
