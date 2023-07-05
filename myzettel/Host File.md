---
template: note
---
![tp.web.random_picture](https://images.unsplash.com/photo-1633461935744-530490c7cd85?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjY1NTUxMzgy&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-10-12) | (time:: 10:39) | (weather:: Vadodara: ☀️   +29°C ↙7km/h)

# Host File
- The "hosts" file was the first attempt at creating a centrally managed table of computer names and IP addresses.
- This file could be distributed by the Network Administrator and included on the local system.

## File Location
**Windows OS**
```shell
c:\windows\system32\drivers\etc\
```

**Linux**
```shell
/etc/hosts
```

## Open the `Hosts` file
```shell
sudo nano /etc/hosts
```

## Host Entry Format
```
127.0.0.1  localhost
```

## Flush DNS Cache
```shell
sudo killall -HUP mDNSResponder
```

---
## Internal Links
[[2022-10-12]], [[Software Engineering]]