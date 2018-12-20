# VTP

## Convigure VTP

All the switches will be configured to use VTP for VLAN updates. S2 will be configured as the server.Switches S1 and S3 will be configure as clients. They will be in the CCNA VTP domain using the password **admin**.

on the administrator

```text
Configure terminal
vtp domain CCNA
vtp mode server
vtp password admin
```

on the clients

```text
Configure terminal
vtp domain CCNA
vtp mode client
vtp password admin
```

> Verify VTP configurations by entering the `show vtp status` command on all switches

