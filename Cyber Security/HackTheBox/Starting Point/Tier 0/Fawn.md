![[Fawn.png]]
#HackTheBox #Starting-point #VeryEasy 
## Scan Port
For scan port, you can use command `nmap`
```bash
nmap -sC -sV {TARGET IP}
```
## Connecting to Fawn with FTP
FTP stand for File Transfer Protocol
```bash
ftp {TARGET IP}
```
## Find the flag
Login to FTP with username `anonymous` without password. List with `ls` or `dir`. Download the flag with `get`.