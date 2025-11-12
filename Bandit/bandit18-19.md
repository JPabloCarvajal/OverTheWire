# Bandit Level 18 → Level 19

### Level Goal
The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

---

### Solution

```bash
ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO #password of the last level

ssh bandit19@bandit.labs.overthewire.org -p 2220
cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8
```
