# ACL

## ACL

```text
Configure terminal
Access-list 1permit 10.0.5.0 0.0.0.31
Access-list 1 deny any
interface g0/0.10
ip access-group 1 out
Access-list 2 deny 10.0.0.0 0.0.3.255   
Access-list 2 permit any
interface g0/0.20
ip access-group 2 out
```

> show access-list

Standard ACL Syntax

```text
access-list <number> {permit | deny}
```

## ACL numbers

| ACL Numbers |
| :--- |
| 1-99 IP standard1300-1999 |
| 100-199 IP extended2000-2699 |
| 200-299 Protocol |
| 300-399 DECnet |
| 400-499 XNS |
| 500-599 Extended XNS |
| 600-699 Appletalk |
| 700-799 Ethernet MAC |
| 800-899 IPX standard |
| 900-999 IPX extended |
| 1000-1099 IPX SAP |
| 1100-1199 MAC extended |
| 1200-1299 IPX summary |

## Troubleshooting



| Troubleshooting |
| :--- |
| show access-lists \[&lt;number&gt; \| &lt;name&gt;\] |
| show ip access-lists \[&lt;number&gt; \| &lt;name&gt;\] |
| show ip access-lists interface &lt;interface&gt; |
| show ip interface \[&lt;interface&gt;\] |
| show time-range \[&lt;name&gt;\] |



