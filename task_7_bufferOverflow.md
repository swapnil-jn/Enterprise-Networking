# Task 7 - BufferOverflow

### Overwriting the stack remotely

Load the vulnserver into Immunity Debuuger

![](assets/1_running_immunity.jpg)

Spiking 

![](assets/2_sending_generic_tcp.png)

![](assets/3_stat.jpg)

![](assets/4_trun.png)

![](assets/5_trun_crashed.jpg)

### Calculate the location of overwriting

![](assets/1_scr.png)

![](assets/2_crashed.jpg)

![](assets/3_location.png)

### Identify the bad chars

Certain byte characters can cause issues in the development of exploits. We must run every byte through the Vulnserver program to see if any characters cause issues. By default, the null byte\(x00\) is always considered a bad character as it will truncate shellcode when executed. To find bad characters in Vulnserver, we can add an additional variable of “badchars” to our code that contains a list of every single hex character

![](assets/1_script_bad_chars.png)

![](assets/3_chars.jpg)

So, let’s again close/re-open Vulnserver and Immunity Debugger and send this bad boy off. Once you have sent the exploit, you will need to right click on the ESP register and select “Follow in Dump”. You should notice a little bit of movement in the bottom left corner of the program. If you look carefully, you should see all of your bytes in order starting with 01, 02, 03, etc and ending with FF. If a bad character were present, it would seem out of place. Luckily for us, there are no bad characters in the Vulnserver program. Notice below how all of our numbers appear perfect and in order:

![](assets/4_hex_dump_esp.jpg)

Examine this picture below and see if you can identify the bad characters:

![](assets/5_missing_chars.jpg)

### JMP ESP Technique

![](assets/1_load_mona_modules.jpg)

![](assets/2_loaded.jpg)

![](assets/3_nasm_shell.png)

![](assets/4_find.jpg)

![](assets/6.jpg)

### Exploit 

Create a shell code  
As you can see, we generated 351 bytes of shellcode. We need to copy/paste this shellcode into our Python script. 

![](assets/1_script_exploit.png)

Here is what my final script looks like:

![](assets/2_script_exploit.png)

 on designated port

![](assets/3_running.png)

Run the python script

![](assets/6_running_python_script.png)

![](assets/5_running_administrator.jpg)

Gain the shell

![](assets/7_exploit_shell.png)
