![[Dancing.png]]
#HackTheBox #Starting-point #VeryEasy 
## Scan Port
For scan port, you can use `nmap` command
```bash
nmap -sV {TARGET IP} -T4
```
`--min-rate <number>` or `-T<0-5> (higher is faster)` can boost scanning
## Connect to Dancing with SMB/SMBCLIENT/SAMBA
```bash
smbclient -L {TARGET IP}
```
`-L` for get list of shares available on a host
```bash
smbclient -N //{TARGET IP}/SHARENAME
```
`-N` for login without password
## Find the flag
For list, you can use `ls` or `dir`. Download the flag with command `get`.