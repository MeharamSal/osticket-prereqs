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

- Item 5

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
Go through the setup of your virtual machine and make sure the Region is the same as the one previously chosen in Resource group. If you skipped creating a Resource group before, you can create on on the virtual machines page under Create New.
</p>
<br />

<p><img width="1613" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/e510e991-2c14-4531-9b4d-1569bf604a99">

</p>
<p>
Remote Connect into your newly created Virtual Machine once deployed through 'Remote Desktop Connection' located in the start menu of your Windows computer. Copy your virtual machines public IP address and log in with the username you created previously.
</p>
<br />

<p>
<img width="898" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/3e084d21-2723-4841-ba3c-a3fa77f53423">

</p>
<p>
Access your computers control panel and locate Programs. Select 'Turn Windows features on or off'
<p>

  
<img width="331" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/ca8ac071-d026-4018-ae74-4b00f4c8c672">

</p>
<p>
Under Internet Information Services,select 'World Wide Web Services'->Application Development Features ->CGI. Side note: Make sure Common HTTP Features is also selected(right under Application Development Features) <p>







  
<img width="1172" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/43bd0785-be48-4638-83ef-14b5dd5d3203">

</p>
<p>
From the Installation Files, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)

From the Installation Files, download and install the Rewrite Module (rewrite_amd64_en-US.msi)

Create the directory C:\PHP

From the Installation Files, download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP
<p>

  
  
  
  
  
  
<img width="1171" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/6a0f623a-bfab-45a6-8976-a917739384e2">


</p>
<p>
From the Installation Files, download and install VC_redist.x86.exe.
<p>

  
  
  
  
  
  
  
  
 <img width="1193" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/17fff93b-3e28-4cbe-95c4-b1e490ed046c">

</p>
<p>
From the Installation Files, download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
<p>

  
  
  
  
  
 
  
  
 <img width="367" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/15e43278-1b46-4ddd-9085-70cac06fb3e1">

</p>
<p>
Launch Configuration Wizard (after install) ->
Standard Configuration ->
  Set your Password
<p>

  
  
  
  
  
  
  
  
  
  
  
  
  <img width="587" alt="image" src="https://github.com/MeharamSal/osticket-prereqs/assets/173064050/1eb38134-7aeb-4cce-8430-3a9affb19f7b">

</p>
<p>
Run IIS as an Admin
<p>

  
  
  
  
  
  
  
  
  
  
  <img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
text
