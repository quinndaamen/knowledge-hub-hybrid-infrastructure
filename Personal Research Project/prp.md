# PRP - Secure Azure Network Design

## Main Research Question

### How can a secure segmented Azure network architecture be designed and implemented for Fonteyn Holiday Parks to reduce unauthorized lateral movement between services?

---

## Overview

This was my Personal Research Project (PRP) for Fontys in semester 2, where I researched how a secure and well-segmented Azure environment could be designed for Fonteyn Holiday Parks.

This was a project in a team separately from Knowledge Hub, but in terms of what we did, it was similar: designing a hybrid environment for a fictional organization. The main difference this time was that by working in a group we had more professional things to think about, like talking to a stakeholder, but we were also able to dive deeper into a specific part of the network.

For me, this specific part was **Security**.

This documentation is about my PRP, in which I went deeper into the causes and potential solutions for lateral movement.

My main focus was network security and reducing the risk of attackers moving through the infrastructure after gaining initial access.

I researched different security risks and Azure networking components and then used the results to create measures within the architecture for Fonteyn's hybrid environment.

The project also followed professional structures such as PPDIOO by Cisco.

---

## Why I Made This

I had the option to choose whatever research question I wanted, but in the end I settled on this one because it had to do with my main interest, which is Cybersecurity, and it was actually an achievable objective to finish within the timespan of just a few weeks.

I was especially interested in how network segmentation could be used to limit lateral movement and how Azure security services could work together to protect a hybrid environment.

The Fonteyn project also helped me learn how teams work in a bigger project like this, where everyone works simultaneously on a different part of the network to eventually have a fully working environment.

---

## What I Researched

The research focused on several questions:

- What security risks currently exist in insufficiently segmented Azure network environments within Fonteyn Holiday Parks' planned hybrid infrastructure?
- Which Azure networking components are most suitable to securely separate services and environments in Fonteyn Holiday Parks' hybrid cloud architecture?
- How can Zero Trust principles be applied in the current Fonteyn Holiday Parks Azure migration to reduce lateral movement between services?
- How can logging and monitoring improve visibility and threat detection in Fonteyn Holiday Parks' segmented Azure environment?
- How can Infrastructure as Code currently improve the consistency and security of Azure deployments in Fonteyn Holiday Parks' environment?

---

## Research

The research document contains all the research I conducted to eventually create a design that could be implemented to reduce the risks I found.

This was done using the DOT Framework:

https://ictresearchmethods.nl/dot-framework/

[Research Document](PRP%20-%20Research%20Document.docx)

---

## Prepare

In this stage I created requirements, both Functional and Technical, for all the things I had to have implemented in the end to have a finished product.

This included things like:

**TR-03:** Network Security Groups (NSGs) must enforce deny-by-default communication.

**TR-09:** Unauthorized network attempts must be logged and traceable.

Security decisions are based on Zero Trust principles, meaning there is no implicit trust inside the network.

I also defined the Definition of Done in this stage. This sets goals for me to know when I have finished the project.

[Prepare Document](PRP%20-%20Prepare%20Document.docx)

---

## Design

After completing the research, I created a proposed Azure architecture for Fonteyn Holiday Parks.

The design uses:

- Hub-and-Spoke architecture
- A central Hub VNet
- Separate Spoke VNets for different workloads
- Subnet segmentation
- Network Security Groups
- Azure Firewall
- Azure Bastion
- VPN Gateway
- Azure Monitor
- Log Analytics
- NSG Flow Logs
- Infrastructure as Code using Bicep

The design focuses on using the principle of Zero Trust to ensure the possible routes for an attacker are limited.

This is done by segmenting the network and putting NSGs in place which are deny-by-default, so traffic does not automatically flow between different network segments.

[Design Document](PRP%20-%20Design%20Document.docx)

---

## Implementation

This was for me the most fun part: actually building and putting in place the things I had researched and designed in the previous weeks to limit the threat that lateral movement poses to the company.

The basic implementation includes:

### Hub-Spoke Network

**Hub VNet (`vnet-hub`)**

- VPN subnet
  - VPN Gateway to the on-premises GNS3 network
- Bastion subnet
  - Bastion used for access to VMs
- Peering
  - Connected to all Spoke VNets

**Spoke VNet - Reservation**

- Subnet Frontend
  - NSG frontend
- Subnet Backend
  - NSG backend
- Subnet Private Endpoint

**Spoke VNet - Automation**

- Used for Bicep deployment automation

**Spoke VNet - Identity**

- Can later host Active Directory and DNS

**Spoke VNet - IoT**

- Reserved for future IoT systems such as barrier control systems

### Security Measures

**Segmentation per service**

- Through Hub-Spoke
- NSG rules
- Peering
- Subnet segmentation

**Visibility of possible threats**

- Through Virtual Network Flow Logs
- Traffic Analytics

**Minimizing human error during deployment**

- Through using Bicep templates for Infrastructure as Code

**Security principles**

- Zero Trust
- Never Trust, Always Verify
- Least Privilege

---

## What I Learned

This project helped me understand that securing a cloud environment is not just about adding a firewall.

It is about doing research, then creating a design and eventually implementing it. Along the way you learn new things, run into problems and sometimes fail, but that is also where a lot of the learning happens.

I learned how network architecture, segmentation, identity, access control, monitoring and Zero Trust principles all work together.

It also helped me understand how the security decisions made during the design of an infrastructure can directly affect the amount of damage an attacker can cause after gaining initial access.

---

## Project Outcome

The final result of the PRP was a researched and documented design for a more securely segmented hybrid Azure environment.

The project resulted in both a documented security research process and an implemented Azure network design based on the findings from that research.

The PRP also gave me more experience working in a team environment while still allowing me to focus deeply on the security side of the infrastructure.
