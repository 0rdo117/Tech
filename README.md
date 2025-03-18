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
  - HP ProCurve J9146A  
  - Netgear switch (unmanaged) 

### **Servers & Endpoints**  
- **Server**: HP ProLiant DL360p Gen8 (Ubuntu)  
  - **CPU**: Intel Xeon E5-2620 v2 @ 2.10GHz  
  - **RAM**: 80GB (split between processors)  
  - **Storage**: 146GB 10K SAS (expanding soon)  
- **Red Team Machine**: Kali Purple (Hunter)  
- **Security Monitoring**: Security Onion (VM)  

### **Other Components**  
- **Firewall**: pfSense (VM)  
- **Access Point**: WPA2/3 enabled (No built-in firewall)



## Network Configuration  

### **IP Addressing**  
| Device               | IP Address       | Role                  |
|----------------------|------------------|-----------------------|
| Router               | 192.168.1.1      | Gateway               |
| pfSense Firewall     | 192.168.1.2      | Network Segmentation  |
| HP ProCurve Switch   | 192.168.1.3      | Core Switch           |
| Hunter (Kali Purple) | 192.168.1.100    | Red Team Testing      |
| Security Onion (VM)  | 192.168.1.101    | Network Monitoring    |

### **VLANs & Segmentation**  
- **VLAN 10**: Management Network  
- **VLAN 20**: Security Tools  
- **VLAN 30**: Red Team Testing  
- **VLAN 40**: Guest/IoT Devices


## Future Plans & Upgrades  
- [ ] Add an extra hard drive for HP ProLiant DL360p Gen8  
- [ ] Expand memory allocation for Security Onion VM  
- [ ] Test Suricata rule tuning for improved detection  
- [ ] Implement containerized SOC tools for automation  
