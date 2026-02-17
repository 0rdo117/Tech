# Val Skirata Cybersecurity Environment

## Overview

Val Skirata is a personally engineered cybersecurity environment designed to simulate the implementation, validation, and monitoring of security controls within a segmented enterprise-style architecture.

The environment was developed to translate operational Cyber Electromagnetic Activities (CEMA) experience into practical civilian cybersecurity applications aligned with governance, risk management, and continuous monitoring principles.

Rather than serving as a penetration-testing lab, this environment focuses on defensive security engineering, visibility, and control validation using commercially relevant technologies and structured security practices.

## Purpose

The purpose of this environment is to demonstrate how layered security controls can be implemented, observed, and assessed within a controlled infrastructure that mirrors real-world organizational networks.

This project provides a platform to:

- Apply risk-informed security design through network segmentation and boundary protection.
- Implement and evaluate detection and monitoring capabilities across multiple telemetry sources.
- Validate defensive configurations and security visibility using industry-standard tools.
- Simulate continuous monitoring workflows consistent with modern cybersecurity programs.
- Bridge military operational cybersecurity experience with civilian governance, risk, and compliance practices.

Val Skirata is intended to function as a small-scale model of an enterprise security program, emphasizing architecture, monitoring, and control effectiveness rather than offensive tradecraft.


🎯 Objectives:

- Build a secure and segmented lab environment.
- Implement Kali machine for Red Testing.
- Integrate a RedHat-based server for attack automation.
- Deploy Suricata, Snort (via Docker containers) for network monitoring and threat detection.
- Deploy OPNSense Firewall via Virtual Machine for Cyber Lab Firewall.
- Security Onion (VM) for SOC operations.
- Integrate DevSecOps practices for continuous security monitoring and automation.
- Conduct Hydra testing and other red team exercises.


 ## Hardware Overview  

### **Networking Devices**  
- **Router**: OPNSense (VM) (Beskar)
- **Switches**:  
  - HP Pro Curve 2910al-24G-POE (Rex) 
  - Netgear switch (unmanaged) 

### **Servers & Endpoints**  
- **Server**: HP ProLiant DL360 Gen10 (Ubuntu) (Echo)  
  - **CPU**:  Dual Intel Xeon Gold 6130 @ 2.10GHz  
  - **RAM**: 448GB DDR4 (split between processors)  
  - **Storage**: 7.2TB 10K SAS (expanding soon)  
- **Security Monitoring**: Security Onion (VM) (DeathWatch)
- **Honeypot**: Windows 10 (Ordo)
  -
  -
  -

- **Server**: HP ProLiant DL360p Gen8 (Rocky/Alma) (Tech)  
  - **CPU**: Intel Xeon E5-2620 @ 2.10GHz  
  - **RAM**: 112GB DDR3   
  - **Storage**: 146GB 10K SAS (expanding soon)  
- **Red Team Machine**: Kali (Hunter)
   - HP Pavilion
      - AMD Phenom II N620 Dual-Core @2.80 GHz
      - 8GB Ram
      - ~500GB HDD 

### **Other Components**  
- **Firewall**: OPNSense (VM)  
- **Access Point**: WPA2/3 enabled (No built-in firewall)


## Network Configuration  

### **IP Addressing**  
| Device                     | IP Address      | Role                  |
|----------------------------|-----------------|-----------------------|
| Router                     | 192.168.x.1     | Gateway               |
| OPNSense Firewall (VM Echo)| 10.0.x.x        | Network Segmentation  |
| Winodws 10 (Ordo)          | 10.x.x.x        | Honeypot              |
| Hunter (Kali Purple)       | 192.168.x.x     | Red Team Testing      |
| Security Onion (VM Echo)   | 10.x.x.x        | Network Monitoring    |
| IDS Container (Echo)       | 10.x.x.x        | Honeypot Monitor      |
| Tech                       | 192.168.x.x     | Red Team Automation   |
| Echo                       | 10.0.x.x        | Holds SOC             |


### **VLANs & Segmentation**  
- **VLAN 70**: Management Network  
- **VLAN 30**: Honeypot 
- **VLAN 40**: Security Onion
- **VLAN 50**: IDS Container


## Future Plans & Upgrades  
- [ ] Add an extra hard drive for HP ProLiant DL360p Gen8    
- [ ] Implement containerized SOC tools for automation  

