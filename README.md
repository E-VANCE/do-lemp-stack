# LEMP STACK
Setup script for Digital Ocean cloudconfig / metadata on Ubuntu 16.04.x

This file is tested on DigitalOcean. Feel free to contribute on further development and please report issues.

# DIGITALOCEAN INSTALLATION
Use this user script while creating the droplet:

![image](https://cloud.githubusercontent.com/assets/6233650/16084574/04d43c8a-3322-11e6-81f1-a46e31f5728e.png) 

```
#cloud-config
chpasswd:
  list: |
    root: yourrootpassword
  expire: False
runcmd:
- wget https://raw.githubusercontent.com/E-VANCE/do-lemp-stack/master/lemp-16-04.sh
- chmod +x lemp-16-04.sh
- ./lemp-16-04.sh
```

Your password(s) will be stored in /root/mysql_passwd.txt
