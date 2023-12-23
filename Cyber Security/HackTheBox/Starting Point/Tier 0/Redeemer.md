![[Redeemer.png]]
#HackTheBox #Starting-point #VeryEasy 
## Scan Port
```bash
nmap -p- -sV {TARGET IP}
```
`-p <port-ranges>` for specified port
`-p-` for scan port from `1 - 65535`
## Connect to Redeemer with Redis-cli
```bash
redis-cli {TARGET IP}
```
## Find the flag
```bash
//redis-cli//

info //print information
keys <fill> //print key .. use * to print all key
get <fill> //print file key
```

