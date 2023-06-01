Log in to the backup server and switch to the root user:  
``` 
ssh clint@stbkp01 
```  
``` 
sudo su - 
```   

Using the linux ``` sed ``` command, replace all occurances of the string About to Maritime on the XML file /root/nautilus.xml:  

``` 
sed -i 's/About/Maritime/g' /root/nautilus.xml 
```  

Confirm the changes:  
```
cat /root/nautilus.xml | grep Maritime 
```
![image](/images/snap.PNG)