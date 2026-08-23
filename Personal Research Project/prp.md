# PRP - Secure Azure Network Design
## Main research Question
### How can a secure segmented Azure network architecture be designed and implemented for Fonteyn Holiday Parks to reduce unauthorized lateral movement between services?

​

## Overview

This was my Personal Research Project (PRP) for Fontys at semester 2, where I researched
how a secure and well-segmented Azure environment could be designed for
Fonteyn Holiday Parks.

This was a project in a team seperatly to Knowledge hub but in terms of what we did it was he same: Design a Hybrid enviroment for X.  The only thing thtat changed this time was that by working in a group we had more proffesional things to think about like talking to a  Stakeholder but also being able to  dive deeper in a specific part of the Network which ws for me "Security". This documentation is about my PRP document in which i went deeper in the causes and pottential fixes of Lateral Movement

My main focus of the project was network security and reducing the risk of
attackers moving through the infrastructure after gaining initial access(Lateral Movement)

I researched different security risks and Azure networking components and
then used the results to create meaures within the architecture for Fonteyn's hybrid environment.
It also folowes profesional structres like PPDIOO by  Cisco


## Why I Made This

I had the option to chaoose whatever reseach ququastions i wanted but in the end i settled on this one because it had to do with y main interest which is Cybersecurity and it was actually an achievable objective to finish in the timespan of just a few weeks

I was especially interested in how network segmentation could be used to
limit lateral movement and how Azure security services could work together
to protect a hybrid environment.

The Fonteyns h9olliday project also helped me learn how teams work in a bigger project like thi s in which everyone works simentaniouly on a different part of the network to in the end have a fully working enviroment 

## What I Researched

The research focused on several questions:

- What security risks currently exist in insufficiently segmented Azure network environments within Fonteyn Holiday Parks’ planned hybrid infrastructure?​
- Which Azure networking components are most suitable to securely separate services and environments in Fonteyn Holiday Parks’ hybrid cloud architecture?​
- How can Zero Trust principles be applied in the current Fonteyn Holiday Parks Azure migration to reduce lateral movement between services?​
- How can logging and monitoring improve visibility and threat detection in Fonteyn Holiday Parks’ segmented Azure environment?
- How can Infrastructure as Code currently improve the consistency and security of Azure deployments in Fonteyn Holiday Parks’ environment?​​

## Research

The research documrnt contains all research i have condoned to eventusa=ly create an design that can be implemented to reduce my findings. This was done using the DOT framework https://ictresearchmethods.nl/dot-framework/ . 

[Research Document](PRP - Research Document.docx)

## Design

After completing the research, I created a proposed Azure architecture for
Fonteyn Holiday Parks.

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

The Design focuses on using the principle of Zero trust to ensure the possible  routes for an attacker are limited this is done by segmenting the network and putting in place NSGs which are deny-deny by default so no traffic can "flow" between them. 

[Design Document](PRP - Design Document.docx)













## What I Learned

This project helped me understand that securing a cloud environment is not
just about adding a firewall.

I learned how network architecture, segmentation, identity, access control,
monitoring and Zero Trust principles all work together.

It also helped me understand how the security decisions made during the
design of an infrastructure can directly affect the amount of damage an
attacker can cause after gaining initial access.

## Project Outcome

The final result of the PRP was a researched and documented design for a
more securely segmented hybrid Azure environment.

The design was then used as part of the larger Knowledge Hub infrastructure
project and helped me apply the concepts I researched to an actual
infrastructure environment.
