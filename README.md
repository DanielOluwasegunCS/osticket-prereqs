<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used</h2>

- Windows 10 (21H2)

<h2>List of Prerequisites</h2>

- IIS in Windows WITH CGI
- PHP Manager for IIS
- Rewrite Module
- PHP 7.3.8
- Visual Studio Redistribution
- MySQL 5.5.62
- osTicket v1.15.8
- HeidiSQL

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/5MEAasf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I created a Windows 10 virtual machine (VM) with 2 virtual CPUs. When I created this VM, Microsoft Azure also created a virtual network and subnet automatically for me.
</p>
<br />

<p>
<img src="https://i.imgur.com/cJOA5SS.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
I enabled Internet Information Services (IIS) in Windows with CGI because CGI allowed me to install PHP Manager.
</p>
<br />

<p>
<img src="https://imgur.com/bzvnLMh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I downloaded and installed PHP Manager for IIS. osTicket runs off of PHP so later I installed a web server with PHP on this VM.
</p>
<br />

<p>
<img src="https://imgur.com/Kn8weGw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I downloaded and installed an IIS URL Rewrite Module. This is one of the many requirements for osTicket to work.
</p>
<br />

<p>
<img src="https://imgur.com/KliKOPm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I created a directory for PHP on the local C: drive. I then downloaded a zip folder of PHP and extracted it into the PHP folder I made in the C: drive.
</p>
<br />

<p>
<img src="https://imgur.com/V8uiiv8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I downloaded and installed a Microsoft Visual Studio C++ 2015-2022 Redistributable. PHP requires this installation in order for it to work.
</p>
<br />

<p>
<img src="https://imgur.com/Vt7MsSM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I downloaded and installed a MySQL Server Instance Configuration Wizard. This is installing a database on the VM because osTicket needs one in order to store all the application data (tickets, users, agents, etc).
</p>
<br />

<p>
<img src="https://imgur.com/WCPNM31.png" height="90%" width="90%" alt="Disk Sanitization Steps"/>
</p>
<p>
I opened IIS as an admin and registered PHP from within IIS.
</p>
<br />

<p>
<img src="https://imgur.com/Ehl8fFe.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
I downloaded osTicket v1.15.8, copied the "upload" folder to C:\inetpub\wwwroot (webserver's main folder), and renamed the "upload" folder to "osTicket."
</p>
<br />

<p>
<img src="https://imgur.com/rqbZlYx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I enabled PHP extensions. They are reccomendations given by osTicket and improvements for osTicket.
</p>
<br />

<p>
<img src="https://imgur.com/wOefhhQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I allowed all users to have permission to manipulate this file because osTicket has to interact with this file but I don't know which user it will use to do that.
</p>
<br />

<p>
<img src="https://imgur.com/x4uDRke.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After I set up osTicket in the browser I downloaded and installed HeidiSQL. HeidiSQL allowed me to connect to the SQL server that I installed earlier and setup a database that osTicket used.
</p>
<br />

<p>
<img src="https://imgur.com/lUcKAnp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I created a new connection to the MySQL Server. Then I created a new database in HeidiSQL called "osTicket."
</p>
<br />

<p>
<img src="https://imgur.com/BOzICDC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I deleted the setup folder in "C:\inetpub\wwwroot\osTicket", and set permissions to “Read” only in "C:\inetpub\wwwroot\osTicket\include\ost-config.php." After, I browsed to my help desk login page, logged in with my admin account and got on to the ticketing screen.
</p>
<br />
