# Bandit Level 5 → Level 6

### Level Goal
The password for the next level is stored in a file somewhere under the `inhere` directory and has all of the following properties:

* human-readable
* 1033 bytes in size
* not executable

---

### Solution

```bash
ls -la
# search a file that his size must be 1033 bytes (c) 
find inhere/ -type f -size 1033c
cat 'inhere/maybehere07/.file2' # here it is
exit
ssh -p 2220 bandit6@bandit.labs.overthewire.org
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```
