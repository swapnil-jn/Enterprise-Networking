# Task 5 - Metasploit

### Auxiliary Demo

![](assets/1_aux.png)

![](assets/2_aux%20%281%29.png)

![](assets/3_aux.png)

### Exploit Demo

This module exploits the Shellsock vulnerability, a flaw in how the Bash shell handles external environment variables. This module targets CGI scripts in the Apache web server by setting the HTTP\_USER\_AGENT environment variable to a malicious function definition.

![](assets/1_exploit_module_metaspolit.png)

Set the RHOST, TARGETURI and payload. Furthermore, we need to set  LHOST address to the IP address of your machine.

![](assets/2_exploit_module_metasploit.png)

### Payload and types of payloads

[https://www.offensive-security.com/metasploit-unleashed/payloads/](https://www.offensive-security.com/metasploit-unleashed/payloads/)

### Create Payloads

![](assets/1_creating_payloads.png)

![](assets/2_creating_payloads.png)

![](assets/3_creating_payloads.png)

![](assets/4_creating_payloads.png)

### Exploit and its types

{% embed url="https://www.offensive-security.com/metasploit-unleashed/exploits/" %}

### Reverse shell

**Bind Shells**

Bind shells have the listener running on the target and the attacker connect to the listener in order to gain a remote shell.

**Reverse Shells**

Reverse shells have the listener running on the attacker and the target connects to the attacker with a shell.

![](assets/1_reverse_shell.png)

### Bind shells

![](assets/1_bind.png)

![](assets/2_bind_metasploit.png)

![](assets/3_bind_shell_me.png)

![](assets/4_bind_shells_.png)

### Use the database

![](assets/1_db.png)

![](assets/2_db.png)

![](assets/3_db.png)

![](assets/4_db.png)

![](assets/5_db.png)




