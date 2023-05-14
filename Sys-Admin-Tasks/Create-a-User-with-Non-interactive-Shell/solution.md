First, I ssh into App server 3:  
`` ssh banner@stapp03 ``  

Check if the user already exists, using the following command:  
`` id javed ``  

User doesn't exist, so I create a user with a non-interactive shell:   
``  adduser javed  -s /sbin/nologin ``  

I verify if the user has been created successfully:  
`` id javed ``  

![image](/images/L1.PNG)
