SSH into app server 3 and switch to the root user:  
`` ssh banner@stapp03 ``  
`` sudo su - ``  

Check the server Linux distribution:  
`` cat /etc/os-release ``   

Install SELinux:  

`` yum install -y selinux* ``  

Check SELinux status:  
`` sestatus ``    

Edit the config file and change the SELinux status from enforcing to disabled:  
``   vi /etc/selinux/config ``  
     SELINUX=disabled


