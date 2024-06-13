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
First, you will want to create a virtual machine using Azure. To do this go to https://portal.azure.com/. Set up the virtual machine with Windows 10 Pro.

Once created, connect to the virtual machine via Remote Desktop Connection. You will connect the virtual machine by putting its public IP address in.

![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/c1c0c7f3-0405-475e-9f00-fc3e3dcbc37d)


</p>
<p>
Once connected, go to your control panel. From there, open up programs and select Turn Windows features on and off.
</p>
<br />

<p>

  ![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/5bf52089-5096-48ac-845e-78711d501e3c)

  ![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/5f511f06-ea3b-42a1-9726-19434068f1da)





</p>
<p>
After this, you will want to install and enable ISS in Windows with CGI and enable all boxes in Common HTTP Features

![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/30da0cba-bbe9-453d-bc06-6f178f96ccfc)

</p>
<br />
From the Installation Files, Download and Install PHP manager for IIS.
</p>
From the Installtion Files , download and Install the Rewrite Module.
</p>
Create a Folder in the C drive and name it PHP
</p>
From the Installation Files, download PHP 7.3.8 (php-7.3.88-nts-Win32-VC15-x866.zip) and unzip the contents into C:\PHP
</p>
Once you are done with extracting the PHP file in the C drive, download and install the VC_redist.x86exe file.
</p>
From the Installation Files, Download and Install MySQL 5.5.62
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
You will want to open IIS as an Admin. Type IIS in the Windows search browser and it should pop up.

![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/b63128b2-4a8b-47c5-9363-0ced98e70a49)

Click on PHP Manager
</p>

![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/5aed8ccd-22b7-40a6-bb20-07ba86ebc314)
  
Register new PHP version

![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/6c925f74-1249-4668-8092-2e788365999d)

Go back into your C Drive --> PHP --> click on php-cgi file.

![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/14aea22c-eb9f-4cd4-a5a7-4c55763763d0)

Install and download os Ticket v1.15.8

Extract and Copy "Upload" folder to c:\inetpub\wwwroot

Within c:\inetpub\wwwroot, Rename "upload" to "OsTicket"

Reload IIS again.

On IIS click on Sites --> Default --> osTicket. On the right side, hit “Browse *:80”.

![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/d1abaa11-5f86-4926-baba-09a841bf3524)

This will pop up. Some extentions are not enabled.

![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/a433e556-7f65-4250-893a-e6a40aaf5b7a)

Go back to IIS, sites --> Default --> osTicket

Double-click PHP Manager

Click "Enable or disable an extension"

![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/2df3e028-cc93-463c-9a3b-61b68b73490a)

    - Enable: php_imap.dll
</p>    
    - Enable: php_intl.dll
</p>    
    - Enable: php_opcache.dll
Refresh osTicket site in the browser

![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/d11472cb-25e5-46f8-99fd-bd591047a8bb)

After this,  rename one of the files in our osTicket folder. Go into the file explorer and search for C;\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php

![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/0fe27ac4-0413-4099-9e20-b4ab1044dd9d)

Rename the ost-sampleconfig.php to ost-config.php

Assign Permissions: ost-config.php
    - Disable inheritance --> Remove All
   
![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/9e79e598-bbd1-45d0-b6ef-d3966abd337b)

    - New Permissions --> Everyone --> All

![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/39484e70-2229-4a83-afb6-3c8d75829634)

From the Installation Files, download and install HeidiSQL. Finish setting up osticket in the browser. From there everything should be set up.

To clean up, all you have to do is delete the setup file in C:\inetpub\wwwroot\osTicket. Once you do that, go into the "include" file in C:\inetpub\wwwroot\osTicket. From there you are going to change the permissions of the ost-config.php file to "Read" only.

![image](https://github.com/alexhannon/osticket-prereqs/assets/168659572/36bf24a2-c52e-4795-b8fc-576c87bbbe42)

Notes:
  - The help desk login page URL will be HTTP://localhost.osTicket/scp/login.php .
  - The End Users osTicket URL will be: HTTP://localhost/osTicket .
