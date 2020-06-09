# Task 4 - Wireshark & Tcpdump

### \`Interface setup

* Start Wireshark

![](assets/w-1.png)

* Select interface

![](assets/w-2.png)

* Setup

![](assets/w-3.png)

### Protocol Filters

* Http Filter

![](assets/http_1%20%282%29.png)

* TCP filter

![](assets/tcp_1.png)

* With tcpdump

![](assets/1_protocol.png)

### IP Filter

* `ip.src == ip`

![](assets/src-ip.png)

* `ip.dst == ip`

![](assets/dest-ip.png)

* With tcpdump

![](assets/1_ip_src.png)

![](assets/1_ip_dest.png)

### Port Filter

* `tcp.port eq 8080`

![](assets/p-1.png)

* With tcpdump

![](assets/1_http_port_filter.png)

### Credentials stolen

![](assets/http_1.png)

![](assets/http.png)

![](assets/http_3.png)

* tcpdump

![](assets/1_insecure.png)

![](assets/2_insecure.png)
