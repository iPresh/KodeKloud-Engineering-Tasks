SSH to app server 1:
```
ssh tony@stapp01
sudo su -
```

Then find the files and copy with their parent directory into /official as per the task:  

```
find /var/www/html/official -type f -name '*.php' -exec cp --parents {} /official \;
```