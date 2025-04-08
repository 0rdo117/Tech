# Tech:
Cyber Lab for C|ND & C|EH into DevSecOps

📜 Overview

This repository documents the setup and configuration of my Cyber Lab, focused on integrating Certified Network Defender (C|ND) and Certified Ethical Hacker (C|EH) methodologies into a DevSecOps environment.


🎯 Objectives:

- Build a secure and segmented lab environment.
- Implement Kali Purple machine for Red Testing.
- Deploy Suricata, Snort (via Docker containers) for network monitoring and threat detection.
- Deploy pfSense (FreeBSD) via Virtual Machine for Cyber Lab Firewall.
- Security Onion (VM) planned for future implementation.
- Integrate DevSecOps practices for continuous security monitoring and automation.
- Conduct Hydra testing and other red team exercises.


 ## Hardware Overview  

### **Networking Devices**  
- **Router**: Netgear AX4200  
- **Switches**:  
  - HP ProCurve 2910al-24-POE (Rex) 
  - Netgear switch (unmanaged) 

### **Servers & Endpoints**  
- **Server**: HP ProLiant DL360p Gen8 (Ubuntu) (Tech)  
  - **CPU**: Intel Xeon E5-2620 v2 @ 2.10GHz  
  - **RAM**: 80GB DDR3 (split between processors)  
  - **Storage**: 146GB 10K SAS (expanding soon)  
- **Red Team Machine**: Kali Purple (Hunter)  
- **Security Monitoring**: Security Onion (VM) 
- **Server**: HP Proliant DL360 Gen10 (Ubuntu) (Echo)
	-	**CPU**: Dual Intel Xeon Gold 6140 @ 2.30GHz
	- **RAM**: 64GB DDR4 
	- **Storage**: 

### **Other Components**  
- **Firewall**: pfSense (VM)  
- **Access Point**: WPA2/3 enabled (No built-in firewall)


## Network Configuration  

### **IP Addressing**  
| Device              | IP Address      | Role                  |
|---------------------|-----------------|-----------------------|
| Router              | 192.168.x.1     | Gateway               |
| pfSense Firewall (VM)| 192.168.x.2      | Network Segmentation  |
| HP ProCurve Switch   | 192.168.x.3      | Core Switch           |
| Hunter (Kali Purple) | 192.168.x.100    | Red Team Testing      |
| Security Onion (VM)  | 192.168.x.101    | Network Monitoring    |
| Splunk (VM)          | 192.168.x.102    | Log Collection        |


### **VLANs & Segmentation**  
- **VLAN 20**: Management Network  
- **VLAN 30**: Security Tools  
- **VLAN 40**: Red Team Testing  
- **VLAN 50**: Guest/IoT Devices


## Future Plans & Upgrades  
- [ ] Add an extra hard drive for HP ProLiant DL360p Gen8  
- [ ] Expand memory allocation for Security Onion VM  
- [ ] Test Suricata rule tuning for improved detection  
- [ ] Implement containerized SOC tools for automation  
- [ ] Improve on Echo for EMS Project
