# Project Name

Individual infrastructure project growing from an on-premises GNS3 environment into a hybrid Azure architecture

---

## Overview

Explain the project in 1-3 paragraphs.

Include:
- What problem this project solves
- What you built
- The main goal
- Whether it was a personal project, school project, or group project

Example:

This project focuses on designing and implementing a secure infrastructure environment for a fictional organization. The project demonstrates network segmentation, identity management, cloud integration, and security improvements.
This Project focused on researching designing and implementing a infrastructure for a fictional library organisation that had the need to secure be managable, expandable and modernize by using an hybrid architecture. 
This was an School project therefor it was performed in 3 stages:
- On prem using GNS3
    - I implemented the basic infrastructure resources such as:
    - Vlans using a managed Exos Swithc
    - A firewal usingn PFsense
    - WIndows Active Directory
    - File Server with controlled acces using GPO's? and OUs
 
Next stage was to mae the network HGybrid and introduce things such as Monitoring
- Hybrid Using Azure
  - Hub Spoke model for VNets
  - NSGs to limit the traffic flowing between subnets and Vnets
  - IPSEC for a VPN connection betwen the on premise network and the cloud network
  - Monitoring VMs for highger than usual CPU/RAM/Disk usage and alerting ... via emails used by azure monitoring


Stage 3 Modernize the existing monitoring platform into a secure, containerized system. An implementation of IPv6 connectivity, ZTA principles, and a CI/CD pipeline
  - This was the stage where i learned the most due to better research as of before
      - Docker was setup as a way to containorize the montirong scripts for easy deployment on the vms
---

## Technologies Used

### Infrastructure
- 
- 
- 

### Networking
- 
- 
- 

### Security
- 
- 
- 

### Development / Automation
- 
- 
- 

Example:

- Microsoft Azure
- GNS3
- pfSense
- Windows Server
- Active Directory
- Docker
- GitHub Actions
- Python
- Linux CLI
- 

---

## Architecture

(Add architecture diagram/image here)

Brief explanation of the design choices.

Example:

The environment consists of an on-premises network connected with Azure resources. Segmentation is implemented using VLANs, VNets, subnets, and security rules to reduce unauthorized access and lateral movement.

---

## Features / Implementation

List the main things you implemented.

Example:

### Networking
- VLAN segmentation
- Firewall configuration
- Routing between networks
- Network security rules

### Cloud
- Azure Virtual Networks
- Hub-Spoke architecture
- Private endpoints
- Secure remote access

### Identity
- Active Directory
- Entra ID integration
- Role-based access control

### Monitoring
- Logging
- Metrics collection
- Alerting

---

## Security Considerations

Explain the important security decisions.

Example:

- Used least privilege access where possible
- Restricted communication between network segments
- Disabled unnecessary public access
- Applied firewall/security rules based on required communication only

---

## Testing & Validation

Explain how you verified the project worked.

Example:

- Tested allowed and blocked network traffic
- Verified firewall rules
- Checked authentication flows
- Validated service communication
- Tested deployment process

---

## Challenges & Lessons Learned

Talk about real problems.

Example:

- Learned the importance of planning network addressing before deployment
- Improved understanding of cloud networking concepts
- Learned how security decisions impact architecture design

---

## Future Improvements

Things you would improve if continuing.

Example:

- Implement Infrastructure as Code
- Add better monitoring
- Improve automation
- Add additional security controls

---

## Screenshots

(Add important screenshots)

---

## Project Status

Completed / In Development / Archived

---

## Author

Your Name

GitHub: your-profile-link
