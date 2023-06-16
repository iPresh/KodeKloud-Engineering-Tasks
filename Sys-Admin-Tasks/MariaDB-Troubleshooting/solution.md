SSH into the databaser server:
```
ssh peter@stdb01
```

Switch to root user:
```
sudo su -
```

Start mariadb service:
```
systemctl start mariadb
``` 

The service failed to start, so I checked for the status:
```
systemctl status mariadb 
```  

Changed permission to see if it was permission issues:
```
chmod -R 777 /var/run/mariadb
``` 

Restarted the service:
```
systemctl restart mariadb
``` 

Failed to start. Tried setting mysql as owner:
```
chown mysql:mysql /var/run/mariadb
```

Restarted the service:
```
systemctl restart mariadb
``` 

Still failed to start. Had to remove mariadb:
```
yum remove mariadb
```

Removed its files and packages
```
rm -rf /var/lib/mysql
```

Installed mariadb server:
```
yum install mariadb-server
```

Started mariadb service:
```
systemctl start mariadb
``` 

Checked for the status:
```
systemctl status mariadb 
```  

The service was running!