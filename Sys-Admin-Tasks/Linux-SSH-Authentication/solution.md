check if there's an existing ssh key for user thor:  
``` 
ls -al ~/.ssh/id_*.pub
```   

create a new key using the command below:  
```
ssh-keygen -t rsa 
```  

copy this public key to all remote servers for a passwordless connection: 
``` 
    ssh-copy-id tony@stapp01
    ssh-copy-id steve@stapp02  
    ssh-copy-id banner@stapp03  
```    

For above command, here's the syntax:  
``` ssh-copy-id [remote_user]@[server_ip_address] ```  

Now try logging in without passoward to test the password-less ssh connectivity:  
```
ssh tony@stapp01
ssh steve@stapp02
ssh banner@stapp03
```