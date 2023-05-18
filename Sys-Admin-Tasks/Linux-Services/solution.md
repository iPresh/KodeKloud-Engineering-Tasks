SSH into App Server 1  
`` ssh tony@stapp01 ``  
`` sudo su - ``  

Install squid into App Server 1:  
`` yum install squid -y ``   
 
![image](/images/sq1.PNG)  

Start the service and enable its start on boot:  
`` systemctl start squid ``  
`` systemctl enable squid ``  

Check the status of the service:  
`` systemctl status squid ``  

![image](/images/sq2.PNG)  

Repeat the above process on Servers 2 and 3 