# Spanning tree

{% hint style="info" %}
[http://packetlife.net/media/library/11/Spanning\_Tree.pdf](http://packetlife.net/media/library/11/Spanning_Tree.pdf)
{% endhint %}

Het **Spanning Tree** Protocol \(STP - IEEE 802.1D\) wordt gebruikt om redundantie van paden in een netwerktopologie te beheersen. Om netwerken sneller en robuuster te maken worden verbindingen vaak redundant uitgevoerd. Omdat dit kan leiden tot dubbele pakketten wordt het STP gebruikt.

root switch

```text
spanning-tree vlan 1,10,99 root primary
spanning-tree mode rapid-pvst
```

secondary switch

```text
spanning-tree vlan 1,10,99 root secondary
spanning-tree mode rapid-pvst
```

secure laptoppoorten

```text
interface <interface voor pc>
spanning-tree portfast
spanning-tree bpduguard enable
```

> bpduguard enable wordt gebruikt voor het beveiligen voor laptoppoorten

> show spanning-tree
>
> %Warning: portfast should only be enabled on ports connected to a single host. Connecting hubs, concentrators, switches, bridges, etc... to this interface when portfast is enabled, can cause temporary bridging loops. Use with CAUTION



## 

