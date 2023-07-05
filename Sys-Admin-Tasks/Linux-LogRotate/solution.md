Log into app server and switch to root:  
```
ssh tony@stapp01
```
```
sudo su -
```
Update daemon:
```
yum update -y
```

Install httpd as per the task: 
```
yum install httpd -y
```

Check the logrotate folder for existing folders:
```
ll /etc/logrotate.d/
```

```
cat /etc/logrotate.d/httpd
```

Edit the log file following the given instructions:
```
vi /etc/logrotate.d/httpd
```

Add the folowing lines in the file:    
`monthly`  
`rotate 3`


Start the httpd service and check status:
```
systemctl start httpd
```
```
systemctl status httpd
```


Do the same for app servers 2 and 3