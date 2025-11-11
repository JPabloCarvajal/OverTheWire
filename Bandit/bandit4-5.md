# Bandit Level 4 → Level 5

### Level Goal
The password for the next level is stored in the only human-readable file in the `inhere` directory. Tip: if your terminal is messed up, try the "reset" command.

---

### Solution

```bash
ls -la
file inhere/* # The one which file type is ASCII will contain our password
cat './inhere/-file07' # here it is
exit
ssh -p 2220 bandit5@bandit.labs.overthewire.org
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```
