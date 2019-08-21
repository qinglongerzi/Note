## nodejs 8
```
curl -sL https://rpm.nodesource.com/setup_8.x | bash -
yum install -y gcc-c++ make
yum install -y nodejs
node -v
npm -v
```

## nodejs 10
```
curl -sL https://rpm.nodesource.com/setup_10.x | bash -
yum install -y gcc-c++ make
yum install -y nodejs
node -v
npm -v
```

## change version
```
rm -rf /etc/yum.repos.d
rm -rf /var/cache/yum/x86_64/latest/nodesource
# repeat commands mentioned above
```

## install as root
```
# switch to root user
# package will be installed as global with -g option
npm install -g <package-name>
 
# executable file of the package will be installed in /usr/bin and all file of the package will be installed in /usr/lib by default
# we can check global prefix by command as bellow
npm prefix -g
 
# we can change the prefix by command
npm install -g --prefix /your/path <package-name>
```

## install as local user
```
# install in /your/path with --prefix option
npm install -g --prefix /your/path <package-name>
 
# or setup prefix
npm config set prefix /your/path
 
# /your/path can check in .npmrc
# now you can install package in /your/path without --prefix option
npm install -g <package-name>
 
# set path
PATH=$PATH:$HOME/.local/bin:$HOME/bin:$HOME/your/path/bin
```
