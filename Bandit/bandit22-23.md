# Bandit Level 22 → Level 23

### Level Goal
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

---

### Solution

```bash
cat /etc/cron.d/cronjob_bandit23
echo I am user bandit23 | md5sum | cut -d ' ' -f 1 
cat /tmp/8169b67bd894ddbb4412f91573b38db3
exit
ssh bandit23@bandit.labs.overthewire.org -p 2220
0Zf11ioIjMVN551jX3CmStKLYqjk54Ga
```

# fun fact if you put bandit24 on the echo it will give u its password gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8
