```bash
#pt1
show
show domains
show dashboard

workspaces add {NAME}
show workspaces
workspaces select default

show modules
add domains
show domains
add companies
show companies

search {modules}
use {modules}
show info
run

#pt2
show keys
keys add {API NAME} {API}

delete domains {NUM/ROWID}
add domains
show domains

use interesting_files
show info
back

use google_site_web
show info
run // run domain
back

use interesting_files
run // run domain

#pt3
add domains
show domains

use whois_pocs
show info
run // run domain
show contacts
back

use bing_domain_web
show info
run // run domain
show hosts
back

use brute_hosts
show info
run // run domain
show hosts
back

use interesting_files
show info
run // run domain
back

show contacts
show hosts

#pt4
add hosts
use hosts-hosts/resolve
show hosts
run 1
show hosts

use freegeoip
show info
show hosts
run 1-4
back

#pt5
workspaces use default
show keys
add keys {API NAME}{API}

show domains
show hosts

use {API NAME ex: buildwith}
show info
add domains
show domains
run
back
workspaces select default

#pt6
show domains
show hosts
show dashboard

search reporting
use reporting/csv
show info
run
back

use reporting/html
set CUSTOMER BBC
set CUSTOMER Huda
run
```
