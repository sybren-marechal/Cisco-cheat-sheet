# Switch

## configuring basis settings

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

## Configure ip address 

```text
Configure terminal
interface vlan <number Vlan>
ip address <ip addres> <subnet>
no shutdown
ip default-gateway <default-gateway>
exit
```

## Assaning Vlan

```text
Configure terminal
vlan 10
name Students
vlan 20
name Faculty
interface g0/2
switchport mode trunk 
switchport trunk native vlan 99
interface g0/1
switchport mode trunk
interface f0/1
switchport mode access
switchport access vlan 20
```

> vlan 99 = administarters vlan  
> native vlan wordt toegekend op drukste vlan, dit om CPU kracht te besparen.

> Switchport mode **trunk** wordt gebruikt van **switch** naar **switch**  
> Switchport mode **acces** wordt gebruikt van **switch** naar **pc**



