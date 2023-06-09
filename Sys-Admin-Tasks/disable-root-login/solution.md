SSH into app server 1 and switch to root:  
```
ssh tony@stapp01
```

Disable remote login on the server by editing the /etc/ssh/sshd_config file:  
```
/etc/ssh/sshd_config:
	PermitRootLogin no
``` 

For the changes to take effect, restart sshd service:
```
systemctl restart sshd
```

Repeat on app servers 2 and 3.