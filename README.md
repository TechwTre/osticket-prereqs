<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>


<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />
<br />
Part 1: Creating the virtual environment in Azure.<br />
Part 2: Installation of software dependencies and osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Microsoft Azure Active Subscription (Creation of Reasearch Group, VMs, Virtual Networks, Subnets)
- Enable Internet Information Services(IIS)
- PHP Manager
- Rewrite Manager
- C++ Redistributbal
- MySQL Server
- Install osTicket
- Assigning Permissions

<h2>Installation Steps (Part 1) Steps: 1-12</h2>

Step 1: Navigate to "portal.azure.com/#home" to create a Resource Group. Search for Resource Groups. This group will house the Virtual Network and Subnet. 
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/e127feae-1f94-4246-ba86-8e9f061cc551) 
</p>
<br />

Step 2: Click "Create" to create the Resource Group
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/56e0842d-ad3c-4329-ae57-8d6ba48c1952)
</p>
<br />

Step 3: Name the resource group (ex: RG-osTicket). Choose a region. Choose a region close to your primary user base to minimize latency. Also ensure that the region complies with local laws regarding data residency and privacy. Click Review + create.
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/bb95c8b1-94d5-458f-85bd-1363438bf287)
</p>
<br />
