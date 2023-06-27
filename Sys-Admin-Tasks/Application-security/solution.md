SSH into Nautilus's backup server:  
```
ssh clint@stbkp01
sudo su -
``` 

Check the status of the iptables service:  
```
systemctl status iptables
```

Add IPTable rules to open all incoming connections to Nginx's port and block all incoming connections to Apache's port.  
```

iptables -A INPUT -p tcp --dport 8098 -m conntrack --ctstate NEW,ESTABLISHED -j ACCEPT

iptables -A INPUT -p tcp --dport 6300 -m conntrack --ctstate NEW -j REJECT
``` 

Start the iptables service:  
```
systemctl start iptables
```

```
systemctl status iptables
``` 

Save the IPTable rules to make sure they're permanent:  
```
service iptables save
```


View the iptables rules:
```
View Iptable rules
``` 

Test the configuration by connecting to nginx port from the jumpbox server  
```
ping stbkp01:8098
```