# Bandit Level 16 → Level 17

### Level Goal
The credentials for the next level can be retrieved by submitting the password of the current level (kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx) to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL/TLS and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

---

### Solution

```bash
ifconfig
# (scan of server own private ip)
nmap -sV localhost -p 31000-32000
(31790/tcp open  ssl/unknown, 31518/tcp open  ssl/echo)

ncat --ssl localhost 31790
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
#copy the key and on another terminal
nano key #paste the key and save then
chmod 600 key
ssh -i key -p 2220 bandit17@bandit.labs.overthewire.org
```
