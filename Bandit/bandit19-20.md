# Bandit Level 19 → Level 20

### Level Goal
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (`/etc/bandit_pass`), after you have used the setuid binary.

---

### Solution

```bash
ls -la
./bandit20-do whoami
./bandit20-do ls /etc/bandit_pass
./bandit20-do cat /etc/bandit_pass/bandit20 # here it is
exit
ssh bandit20@bandit.labs.overthewire.org -p 2220
0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
```