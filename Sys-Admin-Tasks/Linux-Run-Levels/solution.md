SSH into the app server and switch to root user:  
```
ssh tony@stapp01
sudo su - 
```

Find the current default linux run level:  
```
systemctl get-default
```

Change from multi-user to graphical target:  
```
systemctl set-default graphical.target
```

Repeat on other app servers.

![image](/images/gui.PNG)