<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- Internet Information Services (IIS)  
- PHP Manager
- Rewrite Module
- VC Redist
- MySQL
- osTicketv1.15.8
- Link to downloads: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

<h2>Installation Steps</h2>

<p>
1. First, you will want to create a virtual machine using Azure. To do this go to https://portal.azure.com/. Set up the virtual machine with Windows 10 Pro.

2. Once created, connect to the virtual machine via Remote Desktop Connection. You will connect the virtual machine by putting its public IP address in.

![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/c1c0c7f3-0405-475e-9f00-fc3e3dcbc37d)


</p>
<p>
3. Once connected, go to your control panel. From there, open up programs and select Turn Windows features on and off.
</p>
<br />

<p>

  ![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/5bf52089-5096-48ac-845e-78711d501e3c)

  ![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/5f511f06-ea3b-42a1-9726-19434068f1da)





</p>
<p>
4. After this, you will want to install and enable ISS in Windows with CGI and enable all boxes in Common HTTP Features

![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/30da0cba-bbe9-453d-bc06-6f178f96ccfc)

</p>
<br />
5. From the Installation Files, Download and Install PHP manager for IIS.
</p>
6. From the Installtion Files , download and Install the Rewrite Module.
</p>
7. Create a Folder in the C drive and name it PHP
</p>
8. From the Installation Files, download PHP 7.3.8 (php-7.3.88-nts-Win32-VC15-x866.zip) and unzip the contents into C:\PHP
</p>
9. Once you are done with extracting the PHP file in the C drive, download and install the VC_redist.x86exe file.
</p>
10. From the Installation Files, Download and Install MySQL 5.5.62
  - Typical Setup -->
</p>
  - Launch Configuration Wizard (after install) -->
</p>
  - Standard Configuration -->
</p>  
  - Set Root Password -->

  ![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/b318099c-e2b4-43f7-86aa-3b9202668e44)
</p>
Then hit Execute to start configuration.
</p>

![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/6f3d2e4b-7274-45db-83cf-66fa81fc801b)

</p>
<p>
11. You will want to open IIS as an Admin. Type IIS in the Windows search browser and it should pop up.

![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/b63128b2-4a8b-47c5-9363-0ced98e70a49)

12. Click on PHP Manager
</p>

![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/5aed8ccd-22b7-40a6-bb20-07ba86ebc314)
  
13. Register new PHP version

![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/6c925f74-1249-4668-8092-2e788365999d)

14.  Go back into your C Drive --> PHP --> click on php-cgi file.

![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/14aea22c-eb9f-4cd4-a5a7-4c55763763d0)

15. Install and download os Ticket v1.15.8
16. Extract and Copy "Upload" folder to c:\inetpub\wwwroot
17. Within c:\inetpub\wwwroot, Rename "upload" to "OsTicket"

Reload IIS again.

14.) On IIS go to sites -> Default -> osTicket -On the right, click “Browse *:80”

</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
