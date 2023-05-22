SSH on app server 1  
`` ssh tony@stapp01 ``  

Install cronie on the server:  
`` sudo yum install -y cronie ``  

Start the cron service:  
`` sudo systemctl start crond.service ``   

Check the status of the cron service:  
`` sudo systemctl status crond.service ``  

Check for any pre-existing cron job:  
`` sudo crontab -l ``  

Create a cron job:  
`` sudo crontab -e ``  

Paste the cron job to the editor:  
`` */5 * * * * echo hello > /tmp/cron_text ``  

Check the cron job:  
`` sudo crontab -l ``  

Check the cron job for root:  
`` sudo crontab -u root -l ``    

Repeat the process for app server 2 and 3


