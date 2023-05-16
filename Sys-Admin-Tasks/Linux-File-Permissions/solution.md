ssh into App server 3:

`` ssh banner@stapp03 ``     
 
Log in as root:  
`` sudo su - ``  

Check the existing file permission for the file using the command below:  
`` ls -ltr /tmp/xfusioncorp.sh ``  

Give every user execute permission:
`` chmod o+rx /tmp/xfusioncorp.sh ``  

Reverify the file permission:  
`` ls -ltr /tmp/xfusioncorp.sh ``  

Exit as root:  
`` exit ``  

Execute the script as user:  
`` sh /tmp/xfusioncorp.sh ``