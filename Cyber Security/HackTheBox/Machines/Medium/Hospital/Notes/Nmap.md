```
# Nmap 7.94 scan initiated Tue Nov 21 13:36:06 2023 as: nmap -A -T4 -oN nmap.txt -vv 10.10.11.241
Nmap scan report for 10.10.11.241 (10.10.11.241)
Host is up, received syn-ack (0.12s latency).
Scanned at 2023-11-21 13:36:06 WIB for 137s
Not shown: 980 filtered tcp ports (no-response)
PORT     STATE SERVICE           REASON  VERSION
22/tcp   open  ssh               syn-ack OpenSSH 9.0p1 Ubuntu 1ubuntu8.5 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   256 e1:4b:4b:3a:6d:18:66:69:39:f7:aa:74:b3:16:0a:aa (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBEOWkMB0YsRlK8hP9kX0zXBlQ6XzkYCcTXABmN/HBNeupDztdxbCEjbAULKam7TMUf0410Sid7Kw9ofShv0gdQM=
|   256 96:c1:dc:d8:97:20:95:e7:01:5f:20:a2:43:61:cb:ca (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIGH/I0Ybp33ljRcWU66wO+gP/WSw8P6qamet4bjvS10R
53/tcp   open  domain            syn-ack Simple DNS Plus
88/tcp   open  kerberos-sec      syn-ack Microsoft Windows Kerberos (server time: 2023-11-21 13:36:34Z)
135/tcp  open  msrpc             syn-ack Microsoft Windows RPC
139/tcp  open  netbios-ssn       syn-ack Microsoft Windows netbios-ssn
389/tcp  open  ldap              syn-ack Microsoft Windows Active Directory LDAP (Domain: hospital.htb0., Site: Default-First-Site-Name)
| ssl-cert: Subject: commonName=DC
| Subject Alternative Name: DNS:DC, DNS:DC.hospital.htb
| Issuer: commonName=DC
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2023-09-06T10:49:03
| Not valid after:  2028-09-06T10:49:03
| MD5:   04b1:adfe:746a:788e:36c0:802a:bdf3:3119
| SHA-1: 17e5:8592:278f:4e8f:8ce1:554c:3550:9c02:2825:91e3
| -----BEGIN CERTIFICATE-----
| MIIC+TCCAeGgAwIBAgIQdNv8q6fykq5PQSM0k1YFAjANBgkqhkiG9w0BAQsFADAN
| MQswCQYDVQQDEwJEQzAeFw0yMzA5MDYxMDQ5MDNaFw0yODA5MDYxMDQ5MDNaMA0x
| CzAJBgNVBAMTAkRDMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEA7obA
| P53k1qyTGrYu36d3MfqWRf+nPEFi6i+GK7/8cOoQfQPjPNMMHcmzHaFgkOdAcv12
| jctNzQYh6xUQY5R3zqjXlJyRorftvBlKDU02S4EOKsdytnziHbHG5ZEvRDoCgVH3
| uvt4U7cqwk1uE0r6iWwegK/xxtTVBPkObmepjTO1DEMyj8j6UU9jwyCH8jE5VTCC
| UiWJI/q+B/tcJcINfFerv4oDagptKrMAIfsX+ReqbZojCD5EREjMUyn+AigZTeyS
| ksesM2Cy6fkVkypComklqJw2YIIlDnPxdh3pAwjyUlbcb6WwE5aEKwuEgyRyXHET
| EKwcUBIa7y3iRSVCpQIDAQABo1UwUzAOBgNVHQ8BAf8EBAMCBaAwHgYDVR0RBBcw
| FYICREOCD0RDLmhvc3BpdGFsLmh0YjATBgNVHSUEDDAKBggrBgEFBQcDATAMBgNV
| HRMBAf8EAjAAMA0GCSqGSIb3DQEBCwUAA4IBAQBjA0NUb25R42VBXvb328jEcMam
| 19VS+MPZijp14phJ0Q/YuxlztTGnSlIFrUPWtJWvx8PLtdCnE1MOmFmcS2TNISg9
| Vt1sE4RF5N9s9TeFqCE80wH+qzZMCaBTlQxrzftkTfN67+SxoEGd6aywXEmzG5tw
| wbEe/dMglJVZ0Uk2DUXjpdXIDQlFIg+Yn0CqWjUvppLUyinxpmVqoC5dY8ijuuem
| 3JjZd5mDoYg1XIP3gfAAutdsce5Safoq7oqh0OYb4sQMu0y9YcRL0JsP3cwB4FnW
| eh2XVUa9NjHJi5hvdH3wy6/jU4UwPED41iuM6Y1rwF/l4J0LmELsmmYZEaWm
|_-----END CERTIFICATE-----
443/tcp  open  ssl/http          syn-ack Apache httpd 2.4.56 ((Win64) OpenSSL/1.1.1t PHP/8.0.28)
|_ssl-date: TLS randomness does not represent time
|_http-server-header: Apache/2.4.56 (Win64) OpenSSL/1.1.1t PHP/8.0.28
|_http-title: Hospital Webmail :: Welcome to Hospital Webmail
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
| ssl-cert: Subject: commonName=localhost
| Issuer: commonName=localhost
| Public Key type: rsa
| Public Key bits: 1024
| Signature Algorithm: sha1WithRSAEncryption
| Not valid before: 2009-11-10T23:48:47
| Not valid after:  2019-11-08T23:48:47
| MD5:   a0a4:4cc9:9e84:b26f:9e63:9f9e:d229:dee0
| SHA-1: b023:8c54:7a90:5bfa:119c:4e8b:acca:eacf:3649:1ff6
| -----BEGIN CERTIFICATE-----
| MIIBnzCCAQgCCQC1x1LJh4G1AzANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDEwls
| b2NhbGhvc3QwHhcNMDkxMTEwMjM0ODQ3WhcNMTkxMTA4MjM0ODQ3WjAUMRIwEAYD
| VQQDEwlsb2NhbGhvc3QwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAMEl0yfj
| 7K0Ng2pt51+adRAj4pCdoGOVjx1BmljVnGOMW3OGkHnMw9ajibh1vB6UfHxu463o
| J1wLxgxq+Q8y/rPEehAjBCspKNSq+bMvZhD4p8HNYMRrKFfjZzv3ns1IItw46kgT
| gDpAl1cMRzVGPXFimu5TnWMOZ3ooyaQ0/xntAgMBAAEwDQYJKoZIhvcNAQEFBQAD
| gYEAavHzSWz5umhfb/MnBMa5DL2VNzS+9whmmpsDGEG+uR0kM1W2GQIdVHHJTyFd
| aHXzgVJBQcWTwhp84nvHSiQTDBSaT6cQNQpvag/TaED/SEQpm0VqDFwpfFYuufBL
| vVNbLkKxbK2XwUvu0RxoLdBMC/89HqrZ0ppiONuQ+X2MtxE=
|_-----END CERTIFICATE-----
| tls-alpn: 
|_  http/1.1
|_http-favicon: Unknown favicon MD5: 924A68D347C80D0E502157E83812BB23
445/tcp  open  microsoft-ds?     syn-ack
464/tcp  open  kpasswd5?         syn-ack
593/tcp  open  ncacn_http        syn-ack Microsoft Windows RPC over HTTP 1.0
636/tcp  open  ldapssl?          syn-ack
| ssl-cert: Subject: commonName=DC
| Subject Alternative Name: DNS:DC, DNS:DC.hospital.htb
| Issuer: commonName=DC
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2023-09-06T10:49:03
| Not valid after:  2028-09-06T10:49:03
| MD5:   04b1:adfe:746a:788e:36c0:802a:bdf3:3119
| SHA-1: 17e5:8592:278f:4e8f:8ce1:554c:3550:9c02:2825:91e3
| -----BEGIN CERTIFICATE-----
| MIIC+TCCAeGgAwIBAgIQdNv8q6fykq5PQSM0k1YFAjANBgkqhkiG9w0BAQsFADAN
| MQswCQYDVQQDEwJEQzAeFw0yMzA5MDYxMDQ5MDNaFw0yODA5MDYxMDQ5MDNaMA0x
| CzAJBgNVBAMTAkRDMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEA7obA
| P53k1qyTGrYu36d3MfqWRf+nPEFi6i+GK7/8cOoQfQPjPNMMHcmzHaFgkOdAcv12
| jctNzQYh6xUQY5R3zqjXlJyRorftvBlKDU02S4EOKsdytnziHbHG5ZEvRDoCgVH3
| uvt4U7cqwk1uE0r6iWwegK/xxtTVBPkObmepjTO1DEMyj8j6UU9jwyCH8jE5VTCC
| UiWJI/q+B/tcJcINfFerv4oDagptKrMAIfsX+ReqbZojCD5EREjMUyn+AigZTeyS
| ksesM2Cy6fkVkypComklqJw2YIIlDnPxdh3pAwjyUlbcb6WwE5aEKwuEgyRyXHET
| EKwcUBIa7y3iRSVCpQIDAQABo1UwUzAOBgNVHQ8BAf8EBAMCBaAwHgYDVR0RBBcw
| FYICREOCD0RDLmhvc3BpdGFsLmh0YjATBgNVHSUEDDAKBggrBgEFBQcDATAMBgNV
| HRMBAf8EAjAAMA0GCSqGSIb3DQEBCwUAA4IBAQBjA0NUb25R42VBXvb328jEcMam
| 19VS+MPZijp14phJ0Q/YuxlztTGnSlIFrUPWtJWvx8PLtdCnE1MOmFmcS2TNISg9
| Vt1sE4RF5N9s9TeFqCE80wH+qzZMCaBTlQxrzftkTfN67+SxoEGd6aywXEmzG5tw
| wbEe/dMglJVZ0Uk2DUXjpdXIDQlFIg+Yn0CqWjUvppLUyinxpmVqoC5dY8ijuuem
| 3JjZd5mDoYg1XIP3gfAAutdsce5Safoq7oqh0OYb4sQMu0y9YcRL0JsP3cwB4FnW
| eh2XVUa9NjHJi5hvdH3wy6/jU4UwPED41iuM6Y1rwF/l4J0LmELsmmYZEaWm
|_-----END CERTIFICATE-----
1801/tcp open  msmq?             syn-ack
2103/tcp open  msrpc             syn-ack Microsoft Windows RPC
2105/tcp open  msrpc             syn-ack Microsoft Windows RPC
2107/tcp open  msrpc             syn-ack Microsoft Windows RPC
2179/tcp open  vmrdp?            syn-ack
3268/tcp open  ldap              syn-ack Microsoft Windows Active Directory LDAP (Domain: hospital.htb0., Site: Default-First-Site-Name)
| ssl-cert: Subject: commonName=DC
| Subject Alternative Name: DNS:DC, DNS:DC.hospital.htb
| Issuer: commonName=DC
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2023-09-06T10:49:03
| Not valid after:  2028-09-06T10:49:03
| MD5:   04b1:adfe:746a:788e:36c0:802a:bdf3:3119
| SHA-1: 17e5:8592:278f:4e8f:8ce1:554c:3550:9c02:2825:91e3
| -----BEGIN CERTIFICATE-----
| MIIC+TCCAeGgAwIBAgIQdNv8q6fykq5PQSM0k1YFAjANBgkqhkiG9w0BAQsFADAN
| MQswCQYDVQQDEwJEQzAeFw0yMzA5MDYxMDQ5MDNaFw0yODA5MDYxMDQ5MDNaMA0x
| CzAJBgNVBAMTAkRDMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEA7obA
| P53k1qyTGrYu36d3MfqWRf+nPEFi6i+GK7/8cOoQfQPjPNMMHcmzHaFgkOdAcv12
| jctNzQYh6xUQY5R3zqjXlJyRorftvBlKDU02S4EOKsdytnziHbHG5ZEvRDoCgVH3
| uvt4U7cqwk1uE0r6iWwegK/xxtTVBPkObmepjTO1DEMyj8j6UU9jwyCH8jE5VTCC
| UiWJI/q+B/tcJcINfFerv4oDagptKrMAIfsX+ReqbZojCD5EREjMUyn+AigZTeyS
| ksesM2Cy6fkVkypComklqJw2YIIlDnPxdh3pAwjyUlbcb6WwE5aEKwuEgyRyXHET
| EKwcUBIa7y3iRSVCpQIDAQABo1UwUzAOBgNVHQ8BAf8EBAMCBaAwHgYDVR0RBBcw
| FYICREOCD0RDLmhvc3BpdGFsLmh0YjATBgNVHSUEDDAKBggrBgEFBQcDATAMBgNV
| HRMBAf8EAjAAMA0GCSqGSIb3DQEBCwUAA4IBAQBjA0NUb25R42VBXvb328jEcMam
| 19VS+MPZijp14phJ0Q/YuxlztTGnSlIFrUPWtJWvx8PLtdCnE1MOmFmcS2TNISg9
| Vt1sE4RF5N9s9TeFqCE80wH+qzZMCaBTlQxrzftkTfN67+SxoEGd6aywXEmzG5tw
| wbEe/dMglJVZ0Uk2DUXjpdXIDQlFIg+Yn0CqWjUvppLUyinxpmVqoC5dY8ijuuem
| 3JjZd5mDoYg1XIP3gfAAutdsce5Safoq7oqh0OYb4sQMu0y9YcRL0JsP3cwB4FnW
| eh2XVUa9NjHJi5hvdH3wy6/jU4UwPED41iuM6Y1rwF/l4J0LmELsmmYZEaWm
|_-----END CERTIFICATE-----
3269/tcp open  globalcatLDAPssl? syn-ack
| ssl-cert: Subject: commonName=DC
| Subject Alternative Name: DNS:DC, DNS:DC.hospital.htb
| Issuer: commonName=DC
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2023-09-06T10:49:03
| Not valid after:  2028-09-06T10:49:03
| MD5:   04b1:adfe:746a:788e:36c0:802a:bdf3:3119
| SHA-1: 17e5:8592:278f:4e8f:8ce1:554c:3550:9c02:2825:91e3
| -----BEGIN CERTIFICATE-----
| MIIC+TCCAeGgAwIBAgIQdNv8q6fykq5PQSM0k1YFAjANBgkqhkiG9w0BAQsFADAN
| MQswCQYDVQQDEwJEQzAeFw0yMzA5MDYxMDQ5MDNaFw0yODA5MDYxMDQ5MDNaMA0x
| CzAJBgNVBAMTAkRDMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEA7obA
| P53k1qyTGrYu36d3MfqWRf+nPEFi6i+GK7/8cOoQfQPjPNMMHcmzHaFgkOdAcv12
| jctNzQYh6xUQY5R3zqjXlJyRorftvBlKDU02S4EOKsdytnziHbHG5ZEvRDoCgVH3
| uvt4U7cqwk1uE0r6iWwegK/xxtTVBPkObmepjTO1DEMyj8j6UU9jwyCH8jE5VTCC
| UiWJI/q+B/tcJcINfFerv4oDagptKrMAIfsX+ReqbZojCD5EREjMUyn+AigZTeyS
| ksesM2Cy6fkVkypComklqJw2YIIlDnPxdh3pAwjyUlbcb6WwE5aEKwuEgyRyXHET
| EKwcUBIa7y3iRSVCpQIDAQABo1UwUzAOBgNVHQ8BAf8EBAMCBaAwHgYDVR0RBBcw
| FYICREOCD0RDLmhvc3BpdGFsLmh0YjATBgNVHSUEDDAKBggrBgEFBQcDATAMBgNV
| HRMBAf8EAjAAMA0GCSqGSIb3DQEBCwUAA4IBAQBjA0NUb25R42VBXvb328jEcMam
| 19VS+MPZijp14phJ0Q/YuxlztTGnSlIFrUPWtJWvx8PLtdCnE1MOmFmcS2TNISg9
| Vt1sE4RF5N9s9TeFqCE80wH+qzZMCaBTlQxrzftkTfN67+SxoEGd6aywXEmzG5tw
| wbEe/dMglJVZ0Uk2DUXjpdXIDQlFIg+Yn0CqWjUvppLUyinxpmVqoC5dY8ijuuem
| 3JjZd5mDoYg1XIP3gfAAutdsce5Safoq7oqh0OYb4sQMu0y9YcRL0JsP3cwB4FnW
| eh2XVUa9NjHJi5hvdH3wy6/jU4UwPED41iuM6Y1rwF/l4J0LmELsmmYZEaWm
|_-----END CERTIFICATE-----
3389/tcp open  ms-wbt-server     syn-ack Microsoft Terminal Services
| rdp-ntlm-info: 
|   Target_Name: HOSPITAL
|   NetBIOS_Domain_Name: HOSPITAL
|   NetBIOS_Computer_Name: DC
|   DNS_Domain_Name: hospital.htb
|   DNS_Computer_Name: DC.hospital.htb
|   DNS_Tree_Name: hospital.htb
|   Product_Version: 10.0.17763
|_  System_Time: 2023-11-21T13:37:39+00:00
| ssl-cert: Subject: commonName=DC.hospital.htb
| Issuer: commonName=DC.hospital.htb
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2023-09-05T18:39:34
| Not valid after:  2024-03-06T18:39:34
| MD5:   0c8a:ebc2:3231:590c:2351:ebbf:4e1d:1dbc
| SHA-1: af10:4fad:1b02:073a:e026:eef4:8917:734b:f8e3:86a7
| -----BEGIN CERTIFICATE-----
| MIIC4jCCAcqgAwIBAgIQJ8MSkg5FM7tDDww5/eWcbjANBgkqhkiG9w0BAQsFADAa
| MRgwFgYDVQQDEw9EQy5ob3NwaXRhbC5odGIwHhcNMjMwOTA1MTgzOTM0WhcNMjQw
| MzA2MTgzOTM0WjAaMRgwFgYDVQQDEw9EQy5ob3NwaXRhbC5odGIwggEiMA0GCSqG
| SIb3DQEBAQUAA4IBDwAwggEKAoIBAQCsE7CcyqvqUyXdwU9hCSyg21qHJ3DGvSiq
| y9+Afp91IKJd35zkbYgFubrF5F4FLUzcHfcrNdBTw6oFMdNZS5txnjVIQfxoCk1f
| EUnONlIEdi9cattgsEzsNRRG9KJoLrNBIVyYAluMzSoaFF5I0lhSWTlv0ANsdTHz
| rzsc8Avs6BkKLsc03CKo4y3h+dzjWNOnwD1slvoA/IgoiJNPSlrHD01NPuD2Q93q
| 5Yr1mlbx9aew2M4gsEH1YO8k6JfTmVQNLApOVlhlRP/Ak2ZBCJz74UWagufguTSG
| dC/ucQHwe3K7qMD+DpxhMm5XaupkQFvxZdb6fQ8f8wgS6RhM/Ph9AgMBAAGjJDAi
| MBMGA1UdJQQMMAoGCCsGAQUFBwMBMAsGA1UdDwQEAwIEMDANBgkqhkiG9w0BAQsF
| AAOCAQEAXe9RRGaMAiYnxmhDqbb3nfY9wHPmO3P8CUgzWvA0cTKSbYEb5LCA0IBK
| 7v8svFcAQM94zOWisTu54xtuSiS6PcHfxYe0SJwl/VsZm52qt+vO45Zao1ynJdw/
| SnIeAIKktpq8rZZumYwy1Am65sIRZgw2ExFNfoAIG0wJqBDmsj8qcGITXoPUkAZ4
| gYyzUSt9vwoJpTdLQSsOiLOBWM+uQYnDaPDWxGWE38Dv27uW/KO7et97v+zdC+5r
| Dg8LvFWI0XDP1S7pEfIquP9BmnICI0S6s3kj6Ad/MwEuGnB9uRSokdttIDpvU4LX
| zXOe5MnTuI+omoq6zEeUs5It4jL1Yg==
|_-----END CERTIFICATE-----
8080/tcp open  http              syn-ack Apache httpd 2.4.55 ((Ubuntu))
| http-title: Login
|_Requested resource was login.php
| http-cookie-flags: 
|   /: 
|     PHPSESSID: 
|_      httponly flag not set
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-open-proxy: Proxy might be redirecting requests
|_http-server-header: Apache/2.4.55 (Ubuntu)
Service Info: Host: DC; OSs: Linux, Windows; CPE: cpe:/o:linux:linux_kernel, cpe:/o:microsoft:windows

Host script results:
|_clock-skew: mean: 6h59m59s, deviation: 0s, median: 6h59m58s
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 23222/tcp): CLEAN (Timeout)
|   Check 2 (port 19979/tcp): CLEAN (Timeout)
|   Check 3 (port 23197/udp): CLEAN (Timeout)
|   Check 4 (port 6176/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled and required
| smb2-time: 
|   date: 2023-11-21T13:37:43
|_  start_date: N/A

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Tue Nov 21 13:38:23 2023 -- 1 IP address (1 host up) scanned in 137.58 seconds
```
first => [[8080]]
second => [[Cyber Security/HackTheBox/Machines/Medium/Hospital/Notes/443]]