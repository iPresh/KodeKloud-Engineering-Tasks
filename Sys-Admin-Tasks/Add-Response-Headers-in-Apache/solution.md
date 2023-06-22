SSH into app server 2 and switch to root:
```
ssh steve@stapp02
``` 
```
sudo su -
``` 

Install httpd as instructed:
```
yum install -y httpd
``` 
Edit the configuration  file and change the Listen port as per the task and also include Header at end:
```
vi /etc/httpd/conf/httpd.conf 
```

`` Listen 3004 ``  

Add the following at the end of the file:
```
Header set X-XSS-Protection "1; mode=block"

Header always append X-Frame-Options SAMEORIGIN

Header set X-Content-Type-Options nosniff
```  

Create an index.html file with the assigned content:

```
vi /var/www/html/index.html
``` 

Welcome to the xFusionCorp Industries!     

Start the httpd service and also check the status:

```
systemctl start httpd
```
```
systemctl status httpd
```

Test using curl on the given app server:
```
curl http://localhost:3004
``` 

```
curl -i http://localhost:3004
``` 


![image](/images/apache-header.PNG)
