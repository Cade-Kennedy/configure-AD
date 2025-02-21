<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Set Up an Azure Virtual Network
- Deploy a Windows Server Virtual Machine
- Install and Configure Active Directory Domain Services

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/rdmCR1A.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Firstly we are going to create a VNet within Microsoft Azure. This will be The Virtual Network (VNet) used to provide a secure and isolated network environment for deploying Active Directory (AD). It acts as the foundation for network communication between domain controllers, client machines, and other Azure resources.
</p>
<br />

<p>
<img src="https://i.imgur.com/zSCDvTW.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we have the Virtual Machine (VM) that we will be using. This Virtual Machine serves as a Domain Controller (DC), which is responsible for managing authentication, security policies, and directory services.

- We will need to configure some network settings for the domain controller within Microsoft Azure. To locate these settings follow these steps. Virtual Machine/Networking/Network settings/Network interface/Ipconfig/Private ip allocation. Change setting from dynamic to static. 
</p>
<br />

<p>
<img src="https://i.imgur.com/T89kpRR.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here we are configuring settings on the main Domain Controller. We are going to begin configuring the server by enabling Active Directory Domain and Services. 

  - You will need to configure a new domain to actually have a domain on your server. To do this locate the Active Directory Domain Configuration Services, and select "add new forest" here you can name your domain and select continue. 
</p>
<br />
