# download tool
https://github.com/certbot/certbot

# get new crt
./certbot-auto certonly --agree-tos -m email@x.x.x --webroot -w /the/path/of/website -d domain

# renew
./certbot-auto renew --post-hook "service httpd restart"

# crontab
- create a new script auto-renew.sh

#!/bin/bash
PATH=/sbin:/bin:/usr/bin
/root/certbot-master/certbot-auto renew --post-hook "service httpd restart" > /dev/null 2>&1
