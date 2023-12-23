![[Appointment.png]]
#HackTheBox #Starting-point #VeryEasy 
## Scan Port
To scan port, we can use `nmap` command
```bash
nmap -sC -sV -T4 {TARGET IP}
```
`-sC` scan script
`-sV` print with version
`-T4` boost speed scanning port
We can get port `443/tcp`, that's https protocol
## Login to Appointment with Browser
First, open your browser and paste `TARGET IP`. Then the result is a Login Website. 
```http
http://{TARGET IP}
```
![[Appointment-web1.png]]
To be able to login, you can use `SQL INJECTION` with the username `admin'#`, and the password is up to you. Congratulations! you got the flag!!

![[Appointment-web2.png]]