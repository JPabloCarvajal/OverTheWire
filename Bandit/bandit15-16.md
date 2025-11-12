# Bandit Level 15 → Level 16

### Level Goal
The password for the next level can be retrieved by submitting the password of the current level to port `30001` on `localhost` using SSL/TLS encryption.

---

### Solution

```bash
openssl s_client -connect localhost:30001
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo   # submit the password of the current level

exit
ssh -p 2220 bandit16@bandit.labs.overthewire.org
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
```
