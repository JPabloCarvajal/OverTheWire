# Bandit Level 21 → Level 22

### Level Goal
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in `/etc/cron.d/` for the configuration and see what command is being executed.

---

### Solution

```bash
cat /etc/cron.d/cronjob_bandit22
ls /usr/bin/cronjob_bandit22
cat /usr/bin/cronjob_bandit22.sh 
cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv #here it is
exit
ssh bandit22@bandit.labs.overthewire.org -p 2220
tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q
```
