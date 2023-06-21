SSH into app server 1 and switch to root:
```
ssh tony@stapp01
``` 

```
sudo su -
```


Edit the configuration file and change the port as per the task:

```
vi /etc/httpd/conf/httpd.conf
```

`` #Listen 12.34.56.78:80 ``  
``Listen 3003 ``  



To add some permanent & temporary redirects, create a main.conf: 

```
vi /etc/httpd/conf.d/main.conf

```

Add the following to the file:


```
<VirtualHost *:3003>
ServerName http://stapp01.stratos.xfusioncorp.com:3003/
Redirect 301 / http://www.stapp01.stratos.xfusioncorp.com:3003/
</VirtualHost>

<VirtualHost *:3003>
ServerName  http://www.stapp01.stratos.xfusioncorp.com:3003/blog/
Redirect 302 /blog/ http://www.stapp01.stratos.xfusioncorp.com:3003/news/
</VirtualHost>

```

Restart httpd service:
```
systemctl restart httpd
``` 

Check its status:
```
systemctl status httpd
```
