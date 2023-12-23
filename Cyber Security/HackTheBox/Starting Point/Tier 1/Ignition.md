## Nmap
```
PORT   STATE SERVICE REASON         VERSION
80/tcp open  http    syn-ack ttl 63 nginx 1.14.2
| http-methods: 
|_  Supported Methods: GET HEAD POST
|_http-server-header: nginx/1.14.2
|_http-title: Did not follow redirect to http://ignition.htb/
```
## Step
```bash
echo '10.129.189.16 ignition.htb' | sudo tee -a /etc/hosts
```
open browser
```bash
gobuster dir -u {target ip} -w {wordlist}
// or //
feroxbuster -u "target ip"

result :
	---snap---
	/admin
	---snap---
```
open browser, add /admin
```
//user//password//
admin admin123
admin root123
admin password1
admin administrator1
admin changeme1
admin password123
admin qwerty123
admin administrator123
admin changeme123
```
