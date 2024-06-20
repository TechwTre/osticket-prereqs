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


Step 3: Name the resource group (ex: RG-osTicket). Choose a region (Choose a region close to your primary user base to minimize latency). Also ensure that the region complies with local laws regarding data residency and privacy. Click Review + create.
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/bb95c8b1-94d5-458f-85bd-1363438bf287)
</p>
<br />


Step 4: Search for Virtual Machines. Click Create. Select Azure virtual machine.
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/150c1e50-41df-49f1-9568-398f979d1c74)
![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/4880c891-9a8a-4371-891d-9060e30534cf)
</p>
<br />

Step 5: Select the Research Group we created (RG-osTicket). Name the Virtual Machine (ex: VM-osTicket). Choose a Region ex: (US) East US. Choose an image ex: Windows 10 Pro, version 22H2 - x64 Gen2 (free services eligible). 
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/f62e5289-0452-40df-ad01-21681a5966ee)
</p>
<br />

Step 6: Choose a size (ex: Standard_D4s_v3 - 4 vcpus, 16 GiB memory ($140.16/month) note: limited subscriptions cannot use more than 4 vcpus. Choose a Username and Password (Username ex: T-User). Check the Licensing box, and click Next: 
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/6a0a276d-ecbb-4ad5-8c19-fda734d1b7ea)
</p>
<br />

Step 7: Click Next again to navigate to Networking. Azure will create a new Virtual Network and Subnet automatically ex: (new)VM-osTicket-vnet / ex: (new)default(10.0.0.0/24). Click Review + Create
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/6f733c75-c611-49de-aa6e-0accf46f9666)
</p>
<br />

Step 8: Once Validation is passed. Click Create.
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/15c38b90-f2d5-4b97-a537-28f2f0a36c4e)
</p>
<br />

Step 9: When deployment is complete. Navigate to Virtual Machines. Click the (Go to resource) button to see VM information.
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/b66d6434-20f5-4870-a2ac-0ad9b0831304)
</p>
<br />

