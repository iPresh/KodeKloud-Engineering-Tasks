ssh into app server 2 and switch to root:  
```
ssh steve@stapp02
``` 
```
sudo su -
``` 

Create a temporary user names anita:  
```
useradd -e 2021-02-17 anita
```  

Verify the user account expiration details using the ``chage`` command:  

        chage -l anita


![image](/images/tempuser.PNG)