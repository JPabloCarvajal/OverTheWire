# Bandit Level 23 → Level 24

### Level Goal
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

NOTE 2: Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

---

### Solution

```bash
cat /etc/cron.d/cronjob_bandit24
cat /usr/bin/cronjob_bandit24.sh
echo I am user bandit24 | md5sum | cut -d ' ' -f 1
cat /tmp/ee4ee1703b083edac9f8183e4ae70293 #here it is
exit
ssh bandit24@bandit.labs.overthewire.org -p 2220
gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8
```
