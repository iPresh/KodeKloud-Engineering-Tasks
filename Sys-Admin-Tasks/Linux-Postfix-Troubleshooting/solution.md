
Start the postfix service and check the status of postfix using these commands:
```
systemctl start postfix
```

```
systemctl status postfix.service -l
```

![images](/images/ps1.PNG)  


Based on the error, search for inet interfaces:
``` 
cat /etc/postfix/main.cf | grep inet_interfaces
```
![images](/images/ps2.PNG)  



As we've identified the error, edit the configuration file and comment out `` inet_interfaces = localhost``:  
```
vi /etc/postfix/main.cf 
```

![images](/images/ps3.PNG)  


After making the necessary changes, restart the postfix service:
```
sudo systemctl restart postfix
```

Confirm the service is running without any errors:
```
sudo systemctl status postfix
```
![images](/images/ps4.PNG)  
