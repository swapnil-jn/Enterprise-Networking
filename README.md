---
description: NetCat Basics
---

# Task 1

### 1. Connecting & Listening To UDP Port

* On Client Side Run 

```text
netcat -u <target-ip> 2468
```

![](assets/11.png)

* On Server Side Run

```text
netcat -u -l -p 2468
```

![](assets/12.png)

* We can observe the network connection using netstat

```text
netstat | grep 2468
```

![](assets/13.png)

### 2. Connecting & Listening To TCP Port

* On Client Side Run 

```text
netcat -u <target-ip> 1357
```

![](assets/1%20%281%29.png)

* On Server Side Run

![](assets/2%20%281%29.png)

* We can observe the network connection using netstat

```text
netstat | grep 2468
```

![](assets/33.png)

### 3. Transferring Files with Netcat

* On client side run

```text
nc <target_ip> <port> < file_name
```

![](assets/1.png)

* On Server Side Run

```text
nc -l -p <port> file_name
```

![](assets/2.png)

* Can view the file on the target

![](assets/3.png)

### 

