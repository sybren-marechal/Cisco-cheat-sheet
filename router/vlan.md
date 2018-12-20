# VLAN

## intencapsulation dot1Q

This example shows how to enable dot1Q encapsulation on a subinterface for VLAN 30:



```text
Configure terminal
interface g0/0.10
encapsulation dot1Q 10
ip address 10.0.3.1 255.255.252.0
interface g0/0.20
encapsulation dot1Q 20
ip address 10.0.4.1 255.255.255.128
interface g0/0.20
encapsulation dot1Q 99
ip address 10.0.4.1 255.255.255.128
exit
interface g0/0
no shutdown
exit

```

