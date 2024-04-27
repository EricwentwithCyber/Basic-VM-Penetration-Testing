# Basic-VM-Penetration-Testing
This project documents a penetration test performed on a basic virtual machine as part of a penetration testing course. The aim was to identify and exploit vulnerabilities to understand the security posture of the VM.
# Basic VM Penetration Testing

## Tools Used
- ifconfig
- arp
- nmap
- gobuster
- enum4linux
- Hydra
- SSH

## Steps Followed

### Network Scanning
- **ifconfig**: Used to check the network configuration and IP address.
- **ARP**: Command `arp -a` used to find all devices connected to the network.
![Architecture Diagram](https://imgur.com/47nb7fE.jpg)
![Architecture Diagram](https://imgur.com/3FbD8wP.jpg)

### Port Scanning
- **NMAP**: Command `nmap -sV 192.168.56.0/24` used to scan for open ports and running services.
![Architecture Diagram](https://imgur.com/tC3RHkS.jpg)

### Directory Enumeration
- **Gobuster**: Command `sudo gobuster dir -u http://192.168.56.101/ -w /usr/share/wordlists/dirb/common.txt -x .txt,.php,.html` to find directories.
  
![Architecture Diagram](https://imgur.com/GzCrTQ8.jpg)
![Architecture Diagram](https://imgur.com/IVCnEGd.jpg)


### System Enumeration
- **enum4linux**: Used to gather user and system information from the target.
![Architecture Diagram](https://imgur.com/QcY4HcH.jpg)
![Architecture Diagram](https://imgur.com/LtEqNeT.jpg)

### Password Cracking
- **Hydra**: Command `hydra -l jan -P /usr/share/wordlists/rockyou.txt ssh://192.168.56.101` to crack SSH passwords.
![Architecture Diagram](https://imgur.com/Sg6djqr.jpg)

### Privilege Escalation
- Explained methods used to escalate privileges, such as logging in with different user credentials and exploiting sudo vulnerabilities.
![Architecture Diagram](https://imgur.com/wfJaRDi.jpg)
![Architecture Diagram](https://imgur.com/SanTJk4.jpg)

### Post-Exploitation
- Activities performed after gaining access, like directory exploration and capturing flags.
![Architecture Diagram](https://imgur.com/Veb6SDj.jpg)
![Architecture Diagram](https://imgur.com/bnOWOzg.jpg)

![Architecture Diagram](https://imgur.com/GxsbQUN.jpg)

![Architecture Diagram](https://imgur.com/imKXKJM.jpg)
![Architecture Diagram](https://imgur.com/Veb6SDj.jpg)
![Architecture Diagram](https://imgur.com/olgjwuE.jpg)
![Architecture Diagram](https://imgur.com/GlvezXb.jpg)

## Conclusion
Captured the Flag. This VM was my final project for school. After caputring the flag, I ended up with an A+ for the course.
![Architecture Diagram](https://imgur.com/MWGyiF1.jpg)

## Appendix
[Any additional scripts or files used during the testing.
](https://www.vulnhub.com/entry/basic-pentesting-1,216/)
