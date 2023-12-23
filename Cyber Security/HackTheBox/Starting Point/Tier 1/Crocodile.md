![[Crocodile.png]]
#HackTheBox #Starting-point #VeryEasy 
## Scan Port
```bash
nmap -sC -sV {TARGET IP}
```
We get port `21/tcp`, version `vsftpd 3.0.3`. That's FTP service
## Connect to Crocodile with FTP
FTP stand for File Transfer Protocol
```bash
ftp {TARGET IP}

//FTP//
ls
get {file}
```
`ls` for list directory or file
`get` for download the file
```bash
gobuster --url http://{TARGET IP} -w {wordlist} -x {extension file}
```
Later the results will appear login.php. Open your browser, paste TARGET IP, then add login.php at the end of the url
```http
http://{TARGET IP}/login.php
```
Open the two files that were downloaded earlier, in those file there is the username and password.
Congratulations! you get the flag!!