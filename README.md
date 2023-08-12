<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>

<h2>Demonstration</h2>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />





<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Tenant & Subscription
- Resource Group
- Virtual Network
- Subnet
- VM1 in Windows with a NSG

<h2>Installation Steps</h2>

<p>
In Azure, create a Virtual Machine using Windows 10, allow it to create a new Vnet. Name it VM-osTicket.
</p>
<img src="https://i.imgur.com/kKbfhEp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


<p>
Open this file to install all the files we need to support osTicket. (https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)
</p>
<img src="https://i.imgur.com/sy9Qy7B.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>





<p>
First, install IIS in Windows and enable CGI, Common HTTP Featutures, and IIS Management Console.
</p>
<img src="https://i.imgur.com/glmbdek.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>





<p>
Second, download & install PHP Manager for IIS.</p>
<img src="https://i.imgur.com/NdVRZHJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>





<p>
Third, download & install Rewrite Module. </p>
<img src="https://i.imgur.com/Mt3hre7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>





<p>
Fourth, create the directory C://PHP and download PHP 7.3.8 and unzip the contents into the directory you just made.
</p>
<img src="https://i.imgur.com/6yfK6Am.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>





<p>
Fifth, download & install VC_redist.x86_exe.  </p>
<img src="https://i.imgur.com/vOANiP8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>





<p>
Sixth, download & install MYSQL.5.5.62. </p>
<img src="https://i.imgur.com/5odzIfu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>





<p>
Open IIS as an admin and register PHP from within IIS. Then reload IIS. </p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>





<p>
Seventh, install & download osTicket v1.15.8. Extract and copy "upload" folder to c:\inetpub\wwwroot. Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”. Reload IIS. 
 </p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>





<p>
In PHP Manager, enable php_imap.dll, php_intl.dll, and php_opcache.dll. 
 </p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>



<p>
Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

 </p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


<p>
Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All
 </p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>





<p>
Continue setting up osTicket in the browser. </p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>



<p>
Download HeidiSQL and create a new session. Connect to the session and create a database called osTicket.
 </p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


<p>
Continue setting up osTicket in the browser. Enter MYSQL information and Install Now. 
Browse to your help desk login page: http://localhost/osTicket/scp/login.php  
End Users osTicket URL: http://localhost/osTicket/ 
 </p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>





<p>
Congrats! Yous should be able to login to osTicket! </p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>



<br />
