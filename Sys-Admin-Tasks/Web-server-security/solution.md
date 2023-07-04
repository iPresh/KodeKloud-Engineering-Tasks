SSH into the app server and switch to root user:
```
ssh tony@stapp01
sudo su -
```

Edit Apache configuration file:  
```
vi /etc/httpd/conf/httpd.conf
```

For Debian-based systems, edit this file:  
```
/etc/apache2/conf-enabled/security.conf
```

Note: Command for checking your Linux distribution:
```
cat /etc/os-release
```


Append the following values:
```
ServerSignature Off
ServerTokens Prod 
```

Restart httpd service:
```
systemctl restart httpd
```  

Check for HTTP headers:
```
curl -I http://stapp01:8080
```

To Disable the directory browser listing in Apache config: 
```
vi /etc/httpd/conf/httpd.conf
```

Add indexes to Options directive for required directory:
<Directory /var/www/html/>
    Options -Indexes
</Directory>

Restart httpd service:
```
systemctl restart httpd
```
