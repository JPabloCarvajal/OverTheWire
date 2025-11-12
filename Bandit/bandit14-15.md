# Bandit Level 14 → Level 15

### Level Goal
The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

---

### Solution

```bash
# using netcat
nc localhost 30000
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo  # enter the pswd of the last level
# it will show the new password
exit
ssh -p 2220 bandit15@bandit.labs.overthewire.org
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
```
