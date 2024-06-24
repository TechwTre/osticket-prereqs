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

- Microsoft Azure Virtual Machine
- Internet Information Services(IIS)
- PHP Manager
- Rewrite Manager
- C++ Redistributbal
- MySQL (5.5.62) Server
- Heidi SQL
- osTicket v1.15.8
- Assigning Permissions

<h2>Installation Steps (Part 1) Steps: 1-12</h2>

Step 1: Navigate to "portal.azure.com" to create a Resource Group. Search for Resource Groups. This group will house the Virtual Network and Subnet. 
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

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/b93850c9-eae5-4ace-bbb3-0fd89559ae16)
</p>
<br />

Step 11: Copy the Public IP address(ex: 13.77.83.141). Open Remote Desktop Connection. Paste the Public IP address into bar. Click Connect.
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/bf1a491b-49d7-46e3-8c48-99f40f17ae26)
</p>
<br />

Step 12: Enter Username/Password we created in [Step 6] (Username ex: T-User). Click Ok. You should have now launched into your Virtual Enviroment.
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/bba70cd2-1b2d-46db-a4bb-eb93e0c07300)
</p>
<br />

<h2>Installation Steps (Part 2) Steps:  13 - 45</h2>

Step 13: Right click the start menu and select "Run". Type 'control' and hit enter to open the Control Panel.
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/208f1305-31e4-4fba-965a-809202cf4e8e)
![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/60272149-a59f-4f52-a889-6d5e3310921c)
</p>
<br />

Step 14: Click "Programs". Click "Turn Windows features on or off"
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/2ce687a1-c86a-47c2-a83c-2c98ce6cf4c6)
</p>
<br />

Step 15: Check the box for "Internet Information Services". Expand "Internet Information Services". Expand "World Wide Web Services". Expand "Application Development Features". Check the box for "CGI"
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/31630362-a464-49f6-a20b-3833cdf0ae97)
</p>
<br />

Step 16: Collapse "Application Development Features". Expand "Common HTTP Features". Select all boxes and hit ok.
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/164cb7a0-6bcf-48ab-8eab-672814601250)
</p>
<br />

Step 17: Ensure IIS enabling was successful by opening a browser. Enter 127.0.0.1 in the bar. Result should look like this. 
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/bd16f693-07a1-4449-8db1-cbf9d0d38cc7)
</p>
<br />

Step 18: Download and install PHP manager https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view?usp=share_link (PHPManagerForIIS_V1.5.0.msi)
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/fc0c88ac-64d9-486e-bcf8-e2b922ef95d3)
</p>
<br />

Step 19: Download and install the Rewrite Module https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=share_link (rewrite_amd64_en-US.msi)
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/9b417e5d-0b4f-472d-8fc9-c8d77a785e64)
</p>
<br />

Step 20: Navigate to C: drive from File Explorer. Create a new folder called "PHP".
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/e796204e-c978-404d-8653-6cdb0ac98136)
</p>
<br />

Step 21: Download PHP. https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=share_link (php-7.3.8-nts-Win32-VC15-x86.zip). 
  Unzip the contents into C:\PHP
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/b92b8142-2007-4f37-a376-e347ca7aa46a)
</p>
<br />

Step 22: Download and install C++ Redistributable https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=share_link
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/bd6696b0-de60-46e5-84b3-e1013de7b101)
</p>
<br />

Step 23: Download and install MySQL Server. https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view?usp=share_link (mysql-5.5.62-win32.msi). Choose Typical Setup. Choose Standard Configuration. Create a Password
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/8698cf8d-cfa0-44db-80a9-ddc5d999fc73)
![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/f4b3be05-fa07-4d38-956a-48e7ff5ac849)
![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/9e4d3126-b232-4df6-ab3a-8d43dcbadf67)
![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/83962984-232c-4b51-a7f5-55090f4e727e)
</p>
<br />

Step 24: Click Start. Type IIS. RIGHT-click Internet Information Services and choose "Run as Administrator"
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/b760f09e-e094-4637-a4e5-01e6b531fcde)
</p>
<br />

Step 25: Double Click PHP Manager
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/8ba4d40f-441d-4377-8ef7-8cdee6c59cf0)
</p>
<br />

Step 26: Register new PHP version. Provide the path: "php-cgi" inside the PHP folder
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/1da5cdd7-fa4e-4bad-b8f1-df5939b8054d)
</p>
<br />

Step 27: Click the server (ex: VM-osTicket(VM-osTicket\T-user)). Click "Restart" under Manage Server
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/486cffd7-7092-4e2d-9a3e-14b14f1c0c7b)
</p>
<br />

Step 28: Download osTicket. https://drive.google.com/file/d/1cQIErIgsuKE-E-sD_6SO0EBcV9bt4uJh/view?usp=drive_link (v1.15.8). Drag "upload" folder into c:\inetpub\wwwroot 
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/5ac71ea7-ed9d-4417-8d25-6e5b37ce7904)
</p>
<br />

Step 29: Rename "upload" to "osTicket"
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/e1f0b449-d57a-4f7a-8457-637658bfadeb)
</p>
<br />

Step 30: Click "Restart" inside of IIS
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/88221c41-973d-4a2c-a3b2-9cbfdd6b87f6)
</p>
<br />

Step 31: Click the server (ex: VM-osTicket/T-user). Navigate to Sites -> Default Web Site -> click osTicket
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/48a08b8f-587c-485f-b22b-70164b45a85b)
</p>
<br />

Step 32: Click Browse on the right side of IIS, then this window will open
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/4f61b767-e1b5-4c9c-9a2c-78e73e7860ce)
</p>
<br />

Step 33: Double click PHP Manager. Click Enable or disable an extension
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/16e83b1b-d330-46e1-ab93-4fe914da7f72)
</p>
<br />

Step 34: Enable the following: php_imap.dll, php_intl.dll, php_opcache.dll - Refreshing browser should look like this. 
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/33a561c7-1ab6-417a-b066-f440dd36b9ba)
</p>
<br />

Step 35: Navigate to ost-sampleconfig.php then rename this file ost-config.php
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/23ed0ffd-d098-4463-8474-ad8c81b58aae)
</p>
<br />

Step 36: ost-config.php -> Properties -> Security -> Advanced -> Disable inheritance -> Remove all inherited permissions from this object
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/d2306e3d-bfd3-460f-9d4e-956ab036de64)
</p>
<br />

Step 37: Add -> Select a principal -> enter "everyone" in box -> Check Names -> click ok
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/a027fa64-3508-493c-a5d3-1d0feb7b1cf8)
</p>
<br />

Step 38: Give everyone full control -> Press Ok -> Apply -> Ok
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/a7684dcf-d126-4258-aa2b-8d2dd1bae802)
</p>
<br />

Step 39: Click Continue on browser with osTicket open.
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/fb6ab649-ce58-4c3e-989b-a22c69623bfb)
</p>
<br />

Step 40: Download and install Heidi SQL. https://www.heidisql.com/installers/HeidiSQL_12.3.0.6589_Setup.exe This will allow us to connect to the SQL server and set up a database that osTicket will use.
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/88698198-f561-4273-85b6-10b5e42b60f9)
</p>
<br />

Step 41: Click New. Enter User(ex: root) and password. Click Open. This is the connection to the SQL server.
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/74b0e0fc-3d04-41a1-96e5-a4c2f3db4d32)
</p>
<br />

Step 42: Right click "Unnamed" and create a new Database called "osTicket"
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/6961c4db-141e-4ea1-9ea4-dfc910b8a7cb)
</p>
<br />

Step 43: Fill out the osTicket installer form with the data you have chosen and click Install Now.
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/ea5b1936-297e-4982-ad10-a5698717e12b)
</p>
<br />

Step 44: Clean up. Navigate to This PC -> Windows(C:) -> inetpub -> wwwroot -> osTicket and delete the "setup" folder
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/0d9c84de-f726-4d23-a483-a27fce3aef2d)
</p>
<br />

Step 45: Navigate to This PC -> Windows(C:) -> inetpub -> wwwroot -> osTicket -> include -> ost-config.php -> properties -> Security -> Advanced -> Click Everyone -> Edit -> Remove permissions: Full control, Modify, Write -> Ok -> Apply -> Ok -> Ok
</p>

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/73a8ac62-f9df-429a-8682-661711550f90)
</p>
<br />

Installation of osTicket is now complete!    
</p>
<p>
  
![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/94c182d0-df8c-4fa5-a9a9-6c54cc16d871)
</p>
<br />

 URL for ADMIN: http://localhost/osTicket/scp/login.php
</p>
<p>
  URL for end users to create tickets: http://localhost/osTicket/
</p>
<br />

LOGIN as ADMIN will display:
</p>
<br />

![image](https://github.com/TechwTre/osticket-prereqs/assets/126909509/b9733dd6-9d7a-4c64-9ea5-c82e7452d6f5)
</p>





























