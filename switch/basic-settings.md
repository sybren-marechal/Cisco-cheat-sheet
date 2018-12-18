# Basic settings

## configuring basis settings <a id="configuring-basis-settings"></a>

Becoming a super hero is a fairly straight forward process:

```text
Enable
Configure terminal
Hostname S1
no ip domain-lookup
service password-encryption
enable secret admin
banner motd #
Unauthorized access is strictly prohibited. #
line con 0
password admin
login
logging synchronous
line vty 0 15
transport input ssh 
exec-timeout 5 0 
password admin
logging synchronous
login
exit
```

> Password: admin

`show running config`

