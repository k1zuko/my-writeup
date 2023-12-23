![[Keeper.png]]
- nmap
- edit hosts, add keeper.htb n tickets.keeper.htb
- open ur browser
- u can see.. Request tracker, the first before find exploit, search on google request tracker default credential
- u can found login username n password. use that on target
- after login, click admin-user-select tab, u can found lnorgaard n root, we can use lnorgaard, click lnorgaard name section, scroll down until u found password for lnorgaard
- let go to terminal, ssh lnorgaard@ip, n use the password
- ls, u found the user flag
- download zip on another terminal with scp lnorgaard@ip:file.zip ./
- unzip file, result from unzip is pass.kdbx and keepass.dmp
- i found this [poc](https://github.com/CMEPW/keepass-dump-masterkey.git). run keepass.dmp with python n this poc
```bash
python3 poc.py -d keepass.dmp
```
- the result is incorect, lets try to spell it with ggl translate `●ldgr●d med fl●de` del a round one by one.
- after that open the keepass/keepassxc app, open your file pass.kdbx and paste the correct password
- open internet tab and network session, click on root username,the password may not work, see the notes. copy on new file
- because on the note contain putty, lets try use PuTTY
	- session, add host/ip target {keeper.htb}
	- window, selection, turn on auto copy text n ctrl shift c/v
	- connection, ssh, auth, credential, use pass from note earlier
	- fonts, change from server:fixed to the dictionary font
	- run
- login as root
- ls, yuhuu you've got the root flag