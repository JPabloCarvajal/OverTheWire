# Bandit Level 20 → Level 21

### Level Goal
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

NOTE: Try connecting to your own network daemon to see if it works as you think

---

### Solution

```bash
echo -n '0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO' | nc -l -p 1234 &
./suconnect 1234
exit
ssh bandit21@bandit.labs.overthewire.org -p 2220
EeoULMCra2q0dSkYj561DX7s1CpBuOBt
```

credits: https://mayadevbe.me/posts/overthewire/bandit/level21/
