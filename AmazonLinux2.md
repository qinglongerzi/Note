- set timezone
```
timedatectl set-timezone Asia/Tokyo
```

- install nginx
```
amazon-linux-extras list
amazon-linux-extras install nginx1.12
systemctl enable nginx.service
```

- install php
```
amazon-linux-extras list
amazon-linux-extras install php7.2
yum install php <-- php version will be 7.2
```

- remove php
```
yum remove php*
amazon-linux-extras list
amazon-linux-extras disable php7.2
yum install php <-- php version will be 5.4
```
