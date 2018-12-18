# Ethernet Channel



![](../.gitbook/assets/screen-shot-2018-05-22-at-21.33.45.png)



### Configure PAgP

on S1

```text
interface range f0/3-4`
channel-group 1 mode desirable
no shutdown
```

On S3

```text
interface range f0/3-4`
channel-group 1 mode auto
no shutdown
```

> show etherchannel summary

configure trunk ports on both switches

```text
interface port-channel 1
switchport mode trunk
switchport trunk native vlan 99
no shutdown
```

### configure LACP

on s1

```text
interface range f0/1-2
channel-group 1 mode active
no shutdown
```

on S2

```text
interface range f0/1-2
channel-group 1 mode active
no shutdown
```

> show etherchannel
>
> show etherchannel summery

