SSH into App Server 1:
`` ssh tony@stapp01 ``  
`` sudo su - ``  

Delete lines that have the keyword 'code':  

`` sed -e '/code/d' /home/BSD.txt > /home/BSD_DELETE.txt ``  

Replace the keyword 'and' with 'their' making sure this change doesn't affect strings containing the keyword:  

`` sed 's/\<and\>/their/g' /home/BSD.txt > /home/BSD_REPLACE.txt ``