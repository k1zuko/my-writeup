![[Sequel.png]]
#HackTheBox #Starting-point #VeryEasy 
## Scan Port
```bash
nmap -sC -sV {TARGET IP}
```
We can get  port `3306/tcp`, that's mysql service
## Connect to Sequel with MYSQL/MariaDB
```bash
mysql -h {TARGET IP} -u root

//MYSQL/MariaDB//
help;
show databases;
use {database};
show tables;
select * from {table};
```
`-h` command for host
`-u` command for user (user `root` without password)
`help` command for print commands that can you use
`show databases` command for print all databases
`show tables` command for print all databases
`select * from {table}` command for print all contents of the selected table
Congratulations! you got the flag!!
