---
description: nmap
---

# Task 3 - Nmap

### Host Detection

```text
nmap -sP ip
#sP Only Discovery
```

![](assets/1_host.png)

### No Ping Scan

```text
nmap -Pn ip
```

![](assets/1_ping_scan.png)

### Service Version Scan

```text
nmap -sV ip
```

![](assets/service_version.png)

### All Scan

```text
nmap --script vul ip
```

![](assets/1_all_scan.png)

![](assets/2_all_scan.png)

### TCP&UDP scan

```text
nmap -sU -sT -p0-65535 ip
```

![](assets/1_tcp_udp_scan.png)

### Script Engine

#### HTTP

![](assets/1_http.png)

#### Poodle

![](assets/1_poodle.png)

#### Vulner script

![](assets/1_VULNERS.png)

