![[Preignition.png]]
## Nmap
```
PORT   STATE SERVICE REASON         VERSION
80/tcp open  http    syn-ack ttl 63 nginx 1.14.2
| http-methods: 
|_  Supported Methods: GET HEAD
|_http-title: Welcome to nginx!
|_http-server-header: nginx/1.14.2
```
## Step
```bash
gobuster dir -w {wordlist} -u {target ip]
//or//
feroxbuster -u "target ip"

result :
	/admin.php
```
open browser {target ip}/admin.php
login with admin as the username and admin as the password {the flag}