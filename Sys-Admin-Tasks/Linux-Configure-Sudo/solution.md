SSH into app server:
```
ssh tony@stapp01
```

```
sudo su -
```

Check if user exists:
```
id james
``` 

Edit the sudoers, and grant james sudo permission without password:  
```
visudo
```

`` james ALL=(ALL) NOPASSWD=ALL ``