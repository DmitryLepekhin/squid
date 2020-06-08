# How to install and configure Squid

Install squid


```
sudo apt-get update
sudo apt-get install -y squid
# the next command is required to get htpasswd
sudo apt-get install apache2-utils
```


Configure squid.conf
```
# sudo cp /etc/squid/squid.conf /etc/squid/orig.squid.conf
# edit the squid.conf
```

Configure user
```
sudo htpasswd -c /etc/squid/passwords username_your_choice
```

Open port and run
```
sudo ufw allow 3128/tcp
sudo systemctl restart squid.service
```
