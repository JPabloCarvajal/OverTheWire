# Bandit Level 6 → Level 7

### Level Goal
The password for the next level is stored somewhere on the server and has all of the following properties:

* owned by user bandit7
* owned by group bandit6
* 33 bytes in size

---

### Solution

```bash
# we search a file which size is 33bytes (c) owned by bandit7 on the bandit6 group
# we use 2>/dev/null to skip permission error messages. The "2" is stderr (error output).
# "/dev/null" is a place that tells the operating system to ignore it.
# The ">" redirects or sends the error output (stderr) to the ignore location (/dev/null).
find / -type f -size 33c -user bandit7 -group bandit6 2>/dev/null
cat /var/lib/dpkg/info/bandit7.password # here it is
exit
ssh -p 2220 bandit7@bandit.labs.overthewire.org
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
```
