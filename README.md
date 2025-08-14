# Echo:
Cyber Lab for C|ND & C|EH into DevSecOps

📜 Overview

This repository documents the setup and configuration of my Cyber Lab, focused on integrating Certified Network Defender (C|ND)/ Security+ and Certified Ethical Hacker (C|EH) methodologies into a DevSecOps environment. This Lab is for me to gain experience 


🎯 Objectives:

- Build a secure and segmented lab environment.
- Implement Kali machine for Red Testing.
- Integrate a RedHat-based server for attack automation.
- Deploy Suricata, Snort (via Docker containers) for network monitoring and threat detection.
- Deploy pfSense Firewall via Virtual Machine for Cyber Lab Firewall.
- Security Onion (VM) for SOC operations.
- Integrate DevSecOps practices for continuous security monitoring and automation.
- Conduct Hydra testing and other red team exercises.


 ## Hardware Overview  

### **Networking Devices**  
- **Router**: pfSense (VM) 
- **Switches**:  
  - HP Pro Curve 2910al-24G-POE (Rex) 
  - Netgear switch (unmanaged) 

### **Servers & Endpoints**  
- **Server**: HP ProLiant DL360 Gen10 (Ubuntu) (Echo)  
  - **CPU**:  Dual Intel Xeon Gold 6130 @ 2.10GHz  
  - **RAM**: 64GB DDR4 (split between processors)  
  - **Storage**: 7.2TB 10K SAS (expanding soon)  
- **Red Team Machine**: Kali (Hunter)  
- **Security Monitoring**: Security Onion (VM)

- - **Server**: HP ProLiant DL360p Gen8 (Rocky/Alma) (Tech)  
  - **CPU**: Intel Xeon E5-2620 @ 2.10GHz  
  - **RAM**: 112GB DDR3   
  - **Storage**: 146GB 10K SAS (expanding soon)  


### **Other Components**  
- **Firewall**: pfSense (VM)  
- **Access Point**: WPA2/3 enabled (No built-in firewall)


## Network Configuration  

### **IP Addressing**  
| Device              | IP Address      | Role                  |
|---------------------|-----------------|-----------------------|
| Router              | 192.168.x.1     | Gateway               |
| pfSense Firewall (VM)| 10.0.x.x       | Network Segmentation  |
| Winodws 10           | 10.x.x.x       | Honeypot              |
| Hunter (Kali Purple) | 192.168.x.x    | Red Team Testing      |
| Security Onion (VM)  | 10.x.x.x       | Network Monitoring    |
| IDS Container        | 10.x.x.x       | Honeypot Monitor      |
| Tech                 | 192.168.x.x    | Red Team Automation   |
| Echo                 | 10.0.x.x       | Holds SOC             |


### **VLANs & Segmentation**  
- **VLAN 70**: Management Network  
- **VLAN 30**: Honeypot 
- **VLAN 40**: Security Onion
- **VLAN 50**: IDS Container


## Future Plans & Upgrades  
- [ ] Add an extra hard drive for HP ProLiant DL360p Gen8    
- [ ] Implement containerized SOC tools for automation  

