# HSRP Protocol



## HSRP protocol

Hot Standby Router Protocol

![](../.gitbook/assets/screen-shot-2018-05-23-at-20.37.33.png)

In this step, you will configure HSRP and change the default gateway address on PC-A, PC-C, S1, and S2 to the virtual IP address for HSRP. R1 becomes the active router via configuration of the HSRP priority command.

R1

```text
interface g0/1
standby version 2
standby 1 ip <virtual ip>
standby 1 priority 150
standby 1 preempt

```

R2

```text
interface g0/1
standby version 2
standby 1 ip <virtual ip>
```



> show standby
>
> show standby brief

