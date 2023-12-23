![[Meow.png]]
#HackTheBox #Starting-point #VeryEasy
## Scan Port
For scan port, you can use command `nmap`.
```bash
nmap -sC -sV {TARGET IP}
```
`-sC` command for scan script (like directory or some files)
`-sV` command for print version info
## Connecting to Meow with Telnet
For connect to Meow, you can use command `telnet`
```bash
telnet {TARGET IP}
```
## Find the flag
Login to telnet with username `root`. List use `ls`, you got the flag.