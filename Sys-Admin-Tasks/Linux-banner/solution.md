From the Jumphost server, copy the banner to the /tmp directory of all app servers using scp command:  
``` 
scp -r /home/thor/nautilus_banner tony@stapp01:/tmp
scp -r /home/thor/nautilus_banner steve@stapp02:/tmp
scp -r /home/thor/nautilus_banner banner@stapp03:/tmp
```

Log in to each server and switch to root. Then move the nautilus_banner from /tmp to /etc/mod:  
```
  mv /tmp/nautilus_banner /etc/motd
```

For the database server, first install openssh clients package:  
```
ssh peter@stdb01
sudo su -
yum install -y openssh-clients
```  

From the Jump server, copy the banner to the /tmp directory of the DB server:  
```
scp -r /home/thor/nautilus_banner peter@stdb01:/tmp
``` 

Log in to the DB server and move the banner to /etc/mod:  
```
  mv /tmp/nautilus_banner /etc/motd
```

Log in all the servers and check if the banner implemented successfully as per the task