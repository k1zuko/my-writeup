![[Explosion.png]]
## Nmap
```
PORT     STATE SERVICE       REASON          VERSION
135/tcp  open  msrpc         syn-ack ttl 127 Microsoft Windows RPC
139/tcp  open  netbios-ssn   syn-ack ttl 127 Microsoft Windows netbios-ssn
445/tcp  open  microsoft-ds? syn-ack ttl 127
3389/tcp open  ms-wbt-server syn-ack ttl 127 Microsoft Terminal Services
|_ssl-date: 2023-11-27T03:44:01+00:00; -7h59m44s from scanner time.
| rdp-ntlm-info: 
|   Target_Name: EXPLOSION
|   NetBIOS_Domain_Name: EXPLOSION
|   NetBIOS_Computer_Name: EXPLOSION
|   DNS_Domain_Name: Explosion
|   DNS_Computer_Name: Explosion
|   Product_Version: 10.0.17763
|_  System_Time: 2023-11-27T03:43:52+00:00
| ssl-cert: Subject: commonName=Explosion
| Issuer: commonName=Explosion
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2023-11-26T03:39:18
| Not valid after:  2024-05-27T03:39:18
| MD5:   169a:8b36:0b7d:45db:c6a4:940d:d68f:2a20
| SHA-1: b983:28c1:3f2c:fa1a:60d6:13af:9bb5:0249:89dd:b7bc
| -----BEGIN CERTIFICATE-----
| MIIC1jCCAb6gAwIBAgIQGxqyeC0O5oBMi0n2BK1f9jANBgkqhkiG9w0BAQsFADAU
| MRIwEAYDVQQDEwlFeHBsb3Npb24wHhcNMjMxMTI2MDMzOTE4WhcNMjQwNTI3MDMz
| OTE4WjAUMRIwEAYDVQQDEwlFeHBsb3Npb24wggEiMA0GCSqGSIb3DQEBAQUAA4IB
| DwAwggEKAoIBAQC3xjhjiAWGu9LmUBFNzH9f630ajHybUeZBfYqZp55P1VN5wcqD
| OTfjR/31TqzjDIlUHHARjCNPvNGbwTLhCjTHfHO608Y3E7GbRft03CLVEVFKgiUA
| lMfpV8fxk3fZ6GJyuwRsS9vR7lFYcfen+73qMEKF3Gs0wnGjTKzD7evSSWAy2iVi
| kP/8jGVTiSloNhW3rQJf/tzd15P/v13KUznvU7xt8TtY8IRA2W3olucJGEHzduxq
| dK9JoOmtKWnaQyVczntFqy0tF2bqqEWgtJ4f7iSPMmNRNLZQvEyyPOJgieu8GmW2
| Lz2YewK76xC+ynxzOUzgJ2+Cm1UEQ08kezXNAgMBAAGjJDAiMBMGA1UdJQQMMAoG
| CCsGAQUFBwMBMAsGA1UdDwQEAwIEMDANBgkqhkiG9w0BAQsFAAOCAQEAooSCb/GI
| IvqTf/fYzFU+vinv8mVALrYSttAiYBLClSgARTv9G3GlUQIEvfYgnM8P5BQvAB26
| o2YEP9407xhxbvBlIm1cNj85hVrCGIVO2H90ZuEDYgoEHOIDB5CWLn3f0Fj2yfVN
| vPaivDAA6bURXfPxl6ddsTt2ALj2HsQ0YmAD2zzPAa39s6mSlRbR2Len36wKrMRM
| Z57eXtMc7XN5xelU3ALmtnDNeG1W3LG1YCRB0WvnerUIIXX1L2yNSUNEVbKUqkBE
| YcXDpOWMkB+R5dZ94VuoXRFld4nzwVy6HdjxwPBGYEeGO5raT4tk9lt+QiIdmoGn
| Yt/WIX1JWAr5sg==
|_-----END CERTIFICATE-----
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
```
## Step
```bash
xfreerdp /v:10.129.1.13 /cert:ignore /u:Administrator // ===> without password
```