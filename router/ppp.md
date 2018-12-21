# PPP

## CHAP

![](../.gitbook/assets/screenshot-2018-12-18-at-19.58.14.png)

## Debuggin info

```text
debug ppp authentication
debug ppp negotation
debug ppp packet
unbug all
```

Main

```text
username ISP password admin
interface s0/0/0
encapsulation ppp
ppp authentication chap
end


```

ISP

```text
username MAIN password admin
interface s0/0/0
encapsulation ppp
ppp authentication chap
end

```

### troubleshooting

```text
show interfaces s0/0/0
    => Encapsulation PPP, loopback not set, keepalive set (10 sec)
debug ppp packet
debug ppp negotiation
```

