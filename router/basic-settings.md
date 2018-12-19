# Basic Settings

## configure basis settings

```text
Enable
Configure terminal
no ip domain-lookup
hostname R1
service password-encryption
enable secret admin
banner motd #
Unauthorized access is strictly prohibited. #
Line con 0
password admin
login
logging synchronous
line vty 0 4
password admin
login
```

> Password: admin

