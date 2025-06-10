OPEN POWERSHELL RUN ADMINISTRATOR
```php
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
INSTALL CHOCO
```php
choco install mkcert
```
PS C:\WINDOWS\system32> mkcert -install
Created a new local CA 💥
The local CA is now installed in the system trust store! ⚡️

PS C:\WINDOWS\system32> cd 'C:\Users\djamb\'
PS C:\Users\djamb> cd .\Documents\
PS C:\Users\djamb\Documents> mkdir ssl
PS C:\Users\djamb\Documents\ssl> mkcert strukdat.test

Created a new certificate valid for the following names 📜
 - "strukdat.test"

The certificate is at "./strukdat.test.pem" and the key at "./strukdat.test-key.pem" ✅

It will expire on 10 September 2027 🗓

PS C:\Users\djamb\Documents\ssl>
```php
mkcert -install
mkcert strukdat.test
```
ADD HOSTS IN WINDOWS
PS C:\Users\djamb\Documents\ssl> Add-Content -Path "C:\Windows\System32\drivers\etc\hosts" -Value "`n127.0.0.1 strukdat.test"
```php
Add-Content -Path "C:\Windows\System32\drivers\etc\hosts" -Value "`n127.0.0.1 strukdat.test"
```

ADD HOST IN WSL
```php
nano /etc/hosts
```
```php
127.0.0.1 strukdat.test
```
CTRL + x Y enter