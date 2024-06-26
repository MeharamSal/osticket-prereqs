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

- Create a Resource Group
- Create a Windows 10 Virtual Machine (VM) with 2-4 Virtual CPUs
- Install / Enable IIS in Windows WITH
CGI and Common HTTP Features


- Download and Install PHP Manager and Rewrite Module from
             -Files link https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
- From the Installation Files, download and install VC_redist.x86.exe.
- From the Installation Files, download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
- Register PHP from within IIS
- Install osTicket v1.15.8
- Enable extensions
- Assign Permissions: ost-config.php
- Continue Setting up osTicket in the browser
- From the Installation Files, download and install HeidiSQL.
- Continue Setting up osticket in the browser
- Clean up
Delete: C:\inetpub\wwwroot\osTicket\setup
Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php


<h2>Installation Steps</h2>

<p>
<img width="1514" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/c5eaf21d-3592-43fe-a728-6a9764e6b0c8">

</p>
<p>
From the Home page 
  Portal.Azure.com
You will locate Resource Groups and Virtual Machines. (can search for it in search bar if it doesn't Appear)
</p>
<br />

<p>
<img width="789" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/fd84d531-3916-434c-93b0-c29603a19490">

</p>
<p>
Proceed with configuring your virtual machine setup and ensure that the Region matches the one selected earlier for the Resource group. If you did not create a Resource group previously, you can do so on the virtual machines page under 'Create New'</p>
<br />

<p><img width="1613" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/e510e991-2c14-4531-9b4d-1569bf604a99">

</p>
<p>
Access your newly deployed Virtual Machine remotely using 'Remote Desktop Connection' found in the start menu of your Windows computer. Copy the public IP address of your virtual machine and log in using the previously established username
</p>
<br />

<p>
<img width="898" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/3e084d21-2723-4841-ba3c-a3fa77f53423">

</p>
<p>
Access your computer's Control Panel and navigate to Programs. Choose 'Turn Windows features on or off'
<p>

  
<img width="331" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/ca8ac071-d026-4018-ae74-4b00f4c8c672">

</p>
<p>
Navigate to Internet Information Services and select 'World Wide Web Services' -> 'Application Development Features' -> 'CGI'. Ensure that 'Common HTTP Features' is also selected, located directly below 'Application Development Features'.






 <p>







  
<img width="1172" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/43bd0785-be48-4638-83ef-14b5dd5d3203">

</p>
<p>
Download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) from the installation files.

Download and install the Rewrite Module (rewrite_amd64_en-US.msi) from the installation files.

Create the directory C:\PHP.

Download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) from the installation files and extract the contents into C:\PHP.
<p>

  
  
  
  
  
  
<img width="1171" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/6a0f623a-bfab-45a6-8976-a917739384e2">


</p>
<p>
Download and install VC_redist.x86.exe from the installation files.
<p>

  
  
  
  
  
  
  
  
 <img width="1193" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/17fff93b-3e28-4cbe-95c4-b1e490ed046c">

</p>
<p>
Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi) from the installation files.

<p>

  
  
  
  
  
 
  
  
 <img width="367" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/15e43278-1b46-4ddd-9085-70cac06fb3e1">

</p>
<p>
After installation, launch the Configuration Wizard, then choose "Standard Configuration" and set your password.
<p>

  
  
  
  
  
  
  
  
  
  
  
  
  <img width="587" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/1eb38134-7aeb-4cce-8430-3a9affb19f7b">

</p>
<p>
Execute IIS with administrative privileges.
<p>

  
  
  
  
  
  
  
  
  
  <img width="909" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/736292c1-e5e2-4ea6-85ee-bcd0e2fbb97f">
  <img width="794" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/021947d7-ede9-413e-92b6-b02e7534587b">
  <img width="703" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/8c62056c-23e9-412a-99a8-40f327499d37">



</p>
<p>

Register PHP from within IIS











<p>
<img width="936" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/41b7168a-e5d1-4176-bf2b-ccae5745c3eb">

</p>
<p>
Reload IIS (Open IIS, Stop and Start the server)

<p>
<img width="1160" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/2f63f0bf-8b8e-4b14-a6b5-1ed08edd68b2">

</p>
<p>
Install osTicket v1.15.8
Download osTicket from the Installation Files Folder











<p>
<img width="1094" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/2d5bd324-b3b4-4c0c-851d-0e09c2f63e51">

</p>
<p>
Extract the "upload" folder and transfer its contents to c:\inetpub\wwwroot. Subsequently, within c:\inetpub\wwwroot, rename the "upload" directory to "osTicket".

































<p>

</p>
<p>
Reload IIS (Open IIS, Stop and Start the server)
















<p>
<img width="911" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/814c95a6-ff54-4619-aacb-d10aa2b47a0d">

</p>
<p>
Go to sites -> Default -> osTicket
On the right, click “Browse *:80”

























<p>
<img width="611" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/01823d1b-d267-4536-b4cc-ff8c4b77858f">
<img width="620" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/4b806209-8735-4c90-8bc7-024f1c1ab43b">


</p>
<p>
Enable Extensions
















<p>
<img width="235" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/62edcd12-9843-4a6e-84f4-fa5e83ad48e1">
<img width="298" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/9e0cd7c5-e958-4001-a71f-03919e1ee3c4">
<img width="233" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/28328987-eabf-42e5-8d3d-ad2ce8e30893">
<img width="690" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/6347cf05-0076-4acc-8cb7-80309f317937">
  <img width="1184" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/1bd5c01a-f38d-4d2f-8d3c-c93e8e8cc432">





</p>
<p>
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browse, observe the changes

























<p>
<img width="430" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/2b3ef810-7142-461c-a6ed-39d7d0ecddff">
<img width="569" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/35863bbf-bc99-4dea-a7d7-a4cb6040b88a">


</p>
<p>
Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php





























<p>
<img width="404" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/ec858303-8f88-4eb2-a33e-30a5fc773800">
<img width="639" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/eec3e43d-4863-43a5-b82a-6694745fbbae">
<img width="568" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/bbd3b74d-a28f-4220-92b8-02c49f20c5a1">



</p>
<p>
Assign Permissions: ost-config.php
Disable inheritance -> Remove All
























<p>
<img width="674" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/944ba671-6e3b-4f6b-b1b8-90dd3f36625a">
<img width="344" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/c35e3e7e-c046-459a-a534-237dd5f28a9b">
<img width="674" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/7d3c5b86-f54d-46a9-a3c3-a079a8e2e730">
<img width="716" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/8c61b1be-ecf3-4d70-967d-bf72627cb616">






</p>
<p>
New Permissions -> Everyone -> All





























<p>
<img width="919" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/c3fa9c8d-0f4d-4e33-b482-89b8f3a9591d">
<img width="513" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/9e558632-641d-428f-bcfd-babfbfa0de8f">
<img width="286" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/f9f79e1b-46d3-4403-9674-c8c185bea8ea">
<img width="181" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/a468833f-eef4-4c0b-9828-624806dee3e6">




</p>
<p>
From the Installation Files, download and install HeidiSQL.
Open Heidi SQL
Create a new session, Create User and Password
Connect to the session
Create a database called “osTicket”























<p>
<img width="542" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/397cb521-2748-4d30-80a8-e090a77d7565">

</p>
<p>
Proceed with configuring the database settings in osTicket by entering the details for your newly created SQL Database.






















<p>
<img width="747" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/94d20893-68d2-41d6-afe7-bc1adb60a6af">

</p>
<p>
After clicking install you should be met with this page if you followed this guide step by step!




<p>
<img width="769" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/7998bd2f-085c-4251-8804-ef4b77ad19fd">

</p>
<p>
Delete: C:\inetpub\wwwroot\osTicket\setup
Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php










