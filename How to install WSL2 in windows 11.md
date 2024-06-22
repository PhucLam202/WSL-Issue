
#### Computer Configuration
run this line to see check version and status of WSL. Run it on PowerShell or Command Prompt 
```bash
wsl --status
#Default Distribution: Ubuntu-22.04
#Default Version: 2

wsl --version
#WSL version: 2.2.4.0
#Kernel version: 5.15.153.1-2
#WSLg version: 1.0.61
#MSRDC version: 1.2.5326
#Direct3D version: 1.611.1-81528511
#DXCore version: 10.0.26091.1-240325-1447.ge-release
#Windows version: 10.0.22631.3737
```
##### Install 
  Check available distributions
  ```bash
  wsl --list --online
```
   => **Output** 
   ```bash 
#NAME                                   FRIENDLY NAME
#Ubuntu                                 Ubuntu
#Debian                                 Debian GNU/Linux
#kali-linux                             Kali Linux Rolling
#Ubuntu-18.04                           Ubuntu 18.04 LTS
#Ubuntu-20.04                           Ubuntu 20.04 LTS
#Ubuntu-22.04                           Ubuntu 22.04 LTS
#Ubuntu-24.04                           Ubuntu 24.04 LTS
#OracleLinux_7_9                        Oracle Linux 7.9
#OracleLinux_8_7                        Oracle Linux 8.7
#OracleLinux_9_1                        Oracle Linux 9.1
#openSUSE-Leap-15.5                     openSUSE Leap 15.5
#SUSE-Linux-Enterprise-Server-15-SP4    SUSE Linux Enterprise Server 15 SP4
#SUSE-Linux-Enterprise-15-SP5           SUSE Linux Enterprise 15 SP5
#openSUSE-Tumbleweed                    openSUSE Tumbleweed
```

* **NAME:** Short name of the distribution.
* **FRIENDLY NAME:** Full name of the distribution.

Use this command to install version distributions your want 
``` bash
wsl.exe --install --d <NAME>
```
   => In my case, I want download `Ubuntu-22.04` 
```bash 
wsl.exe --install --d Ubuntu-22.04
```
   => Output
```bash 
#Ubuntu 22.04 LTS is already installed.
#Launching Ubuntu 22.04 LTS...
#Installing, this may take a few minutes...
#Please create a default UNIX user account. The username does not need to match your Windows username.
#For more information visit: https://aka.ms/wslusers
#Enter new UNIX username: yor-username
#New password:
#Retype new password:
#passwd: password updated successfully
#Installation successful!
#To run a command as administrator (user "root"), use "sudo <command>".
#See "man sudo_root" for details.

#Welcome to Ubuntu 22.04.3 LTS (GNU/Linux 5.15.153.1-microsoft-standard-WSL2 x86_64) 

 #* Documentation:  https://help.ubuntu.com
 #* Management:     https://landscape.canonical.com
 #* Support:        https://ubuntu.com/advantage


#This message is shown once a day. To disable it please create the
#/home/phuclam/.hushlogin file.
```
>[!NOTE]
>At `New password` and `Retype new password` when you type in the will blank but don't worry it just hidden as you type

To exit Ubuntu windows 
```bash 
exit
```
#### Remove

show all version you got in your divice
```bash
wsl -l -v
```

To remove distributions use Cmd
``` bash
wsl --unregister <NAME>
```
 `Example` 
```bash
wsl --unregister Ubuntu-22.04
```
#### Error and Issue

1. Error : Version Exit
	- If when you ran the Cmd it show you like this
```bash 
C:\Users\ACER>wsl.exe --install --d Ubuntu-22.04
Ubuntu 22.04 LTS is already installed.
Launching Ubuntu 22.04 LTS...
To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.
```
   Don't worry you just need to uninstall the version you got and stall it again
=>Issue 
```bash
wsl --unregister Ubuntu-22.04
```
After this you just installed it again with version of  you want. Good Luck!!!
 