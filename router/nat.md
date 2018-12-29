# NAT

> [http://packetlife.net/media/library/32/NAT.pdf](http://packetlife.net/media/library/32/NAT.pdf)

![](../.gitbook/assets/110-2.jpg)

## NAT

Network Address Translation

```text
Configure terminal
access-list 1 permit 10.0.0.0 0.0.3.255
access-list 1 permit 10.0.4.0 0.0.0.255
ip nat pool publicAcces 1.1.1.2 1.1.1.2 netmask 255.255.255.252 //netwerk op buiten interface
ip nat inside source list 1 pool publicAcces overload
interface g0/0
ip nat inside
interface serial0/0/0
ip nat outside
exit
```

## Troubleshooting

```text
show ip nat translations [verbose]
show ip nat statistics
clear ip nat translations
```



