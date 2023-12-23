```bash
host {DOMAIN/TARGET IP}
host -t ns {DOMAIN/TARGET IP}
host -t mx {DOMAIN/TARGET IP}

nslookup {D/TIP}
nslookup
	set type=ns
	{D/TIP}
	set type=mx
	{D/TIP}
	exit

dig {D/TIP}
dig {D/TIP} -t mx
dig {D/TIP} -t ns
dig {D/TIP} AAAA
dig {D/TIP} CNAME
dig {D/TIP} -t ns +short

for ip in 'dig {D/TIP} +short'; do nmap $ip; done
for ip in 'dig {D/TIP} +short'; do whois $ip; done

host -t ns zonetransfer.me
host -l zonetransfer.me nsztlm.digi.ninja
dig zonetransfer.me -t ns
dig axfr zonetransfer.me @nsztlm.digi.ninja
nslookup
	set type=ns
	zonetransfer.me
dnsrecon -d zonetransfer.me -t axfr
```