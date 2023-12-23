```bash
nmap --help
nmap {DOMAIN/TARGET IP}
nmap -v -A {D/TIP}
nmap -oG - {IP RANGE} -vv > nmap.txt
nmap -oG - {IP RANGE} -p 22 -vv > nmap.txt
nmap -A {D/TIP}
nmap -sV {D/TIP}
nmap -sC {D/TIP}
nmap -F {D/TIP}
nmap -F {D/TIP}{D/TIP} > nmap.txt
nmap --open {D/TIP} > nmap.txt

nslookup {D/TIP}
nslookup {D/TIP} > ns.txt
```
If you don't like use terminal, you can use `Zenmap`