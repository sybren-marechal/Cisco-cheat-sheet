# Vlan

{% hint style="info" %}
[http://packetlife.net/media/library/20/VLANs.pdf](http://packetlife.net/media/library/20/VLANs.pdf)
{% endhint %}

## Assaning Vlan <a id="assaning-vlan"></a>

```text
Configure terminal
vlan 10
name Students
vlan 20
name Faculty
```

### trunk or acces <a id="trunk-or-acces"></a>

```text
interface <g0/2>
switchport mode trunk 
switchport trunk native vlan 99
interface <g0/1>
switchport mode trunk
interface <f0/1>
switchport mode access
switchport access vlan 20
```

> vlan 99 = administarters vlan native vlan wordt toegekend op drukste vlan, dit om CPU kracht te besparen.

> Switchport mode **trunk** wordt gebruikt van **switch** naar **switch of router** Switchport mode **acces** wordt gebruikt van **switch** naar **pc**

Use the **`show vlan brief`** command on all switches to verify that all VLANs are registered in the VLAN table and that the correct ports are assigned. Use the **`show interfaces trunk`** command on all switches to verify trunk interfaces. Use the **`show running-config`** command on all switches to verify all other configurations.

## Delete vlans

```text
delete vlan.dat
reload
```

## Troubleshooting

```text
show vlan
show vlan brief
show interfaces trunk
```



