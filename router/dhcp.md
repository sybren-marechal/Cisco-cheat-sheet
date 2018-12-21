# DHCP

## DHCP

Het DHCP protocol laat ip addressen automatich toekennen.

```text
Configure terminal
ip dhcp excluded-address 10.0.3.1
ip dhcp excluded-address 10.0.3.1 10.0.3.20
ip dhcp pool vlan10
network 10.0.0.0 255.225.252.0
default-router 10.0.3.1
dns-server 8.8.8.8
exit

```

> exlcude-adresses are adresses that will not be used for dhcp

an ip helper is confiugered for  sending the ip adresses trough

```text
Configure terminal
interface g0/0.10
ip helper-address 10.0.5.34
exit
```

> Interface van kant die weg gaat van de DHCP Server.   
> IP Helper IP Address op weg naar DCHP SERVER

