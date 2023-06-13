SSH into app server 2 and switch to root:
```
ssh steve@stapp02
```
```
sudo su -
```

Install ntp on app server 2:
```
yum install -y ntp
``` 

Edit the ntp configuration file:  
`` vi /etc/ntp.conf ``    
```
server 1.sg.pool.ntp.org 
```

