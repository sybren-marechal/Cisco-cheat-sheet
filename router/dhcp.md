---
description: >-
  Dynamic Host Configuration Protocol (DHCP) is een computerprotocol dat
  beschrijft hoe een computer dynamisch zijn netwerkinstelling van een
  DHCP-server kan verkrijgen. Het DHCP-protocol is gebaseerd o
---

# DHCP

## DHCP

Het DHCP protocol laat ip addressen automatich toekennen.

```text
Configure terminal
ip dhcp excluded-address 10.0.3.254
ip dhcp excluded-address 10.0.4.250 10.0.4.254
ip dhcp pool vlan10
network 10.0.0.0 255.225.252.0
default-router 10.0.3.254
exit
ip dhcp pool vlan20
network 10.0.4.0 255.225.255.0
default-router 10.0.4.254
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

## 

