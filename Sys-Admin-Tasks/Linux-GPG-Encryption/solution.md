SSH into storage server and switch to root user:
```
ssh natasha@ststor01
sudo su -
``` 

Go to /home and list all the files located there: 
```
cd /home
ll
```

![images](/images/key1.PNG)

Import GPG Private & Public keys:
```
gpg --import public_key.asc
```

```
gpg --import private_key.asc
```

![images](/images/key2.PNG)

Verify the keys are imported successfully:
```
gpg --list-keys
```
```
gpg --list-secret-keys
``` 
![images](/images/key3.PNG)

Encrypt the file txt into asc as per the task:
```
gpg --encrypt -r kodekloud@kodekloud.com --armor < encrypt_me.txt  -o encrypted_me.asc
``` 

![images](/images/key4.PNG)

Decrypt the file into txt:
```
gpg --decrypt decrypt_me.asc > decrypted_me.txt
``` 

![images](/images/key5.PNG)

Check the encrpyted & decrypted files  in  /home
```
ll
```
![images](/images/key6.PNG)


