
SSH into app server 1:  
```
ssh tony@stapp01 
``` 

Go to the scripts folder and create a script as directed:  
```
vi /scripts/media_backup.sh
```
Below is the content of the script:  

```
#!/bin/bash

zip -r /backup/xfusioncorp_media.zip /var/www/html/media

scp /backup/xfusioncorp_media.zip clint@stbkp01:/backup
```  

Next is to create a create a keygen to make sure the script won't ask for password while copying the archive file.   
Create a keygen and copt the key to the Nautilus backup server:  

```
ssh-keygen
```

Copy the generated key to the backup server:  
```
ssh-copy-id clint@stbkp01
```  

Try to ssh into backup server to ensure it doesn't ask for password:

```
ssh clint@stbkp01
```   

Logout and go the scripts folder (app server 1) and run the bash script:  
```
sh media_backup.sh
``` 

Lastly, confirm that the backup folder for the zip file is saved both on app server 1 and backup server:

```
ll backup
``` 

```
ssh clint@stbkp01
```

```
ll backup
```

The task is done if the folder exists on both servers. 
