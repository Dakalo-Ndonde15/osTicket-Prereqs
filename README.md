<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites]()

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Installation Steps</h2>

- Create an Azure Virtual Machine
- Download the [osTicket-Installation-Files.zip](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD)
- Install / Enable IIS in Windows WITH CGI
- Install PHP Manager for IIS 
- Install the Rewrite Module
- Install [VC_redist.x86.exe.](https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=share_link)
- Install [MySQL 5.5.62](https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view?usp=share_link)
- Install osTicket v1.15.8
- Install [HeidiSQL](https://docs.google.com/document/d/1WovrX2DaS9xkfaSr4LXyB4YnnWpXIgPCMMbbfgHmGVw/edit).
- Set up osTicket in browser


<h2>Project Walk-through:</h2>

<h3>Create Virtual Machine</h3>

<p>
  <img src="https://i.imgur.com/uxTTe2c.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/xIJqzYZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/fJQwhpv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h3>Log into the VM with Remote Desktop</h3>

<p>
  <img src="https://i.imgur.com/BDiFWl0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/f8lkBcs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/5NhPIxP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Within the VM (osticket-vm), download the osTicket-Installation-Files.zip and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files”</h4>

<p>
  <img src="https://i.imgur.com/REB20Yu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/WAy90sq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Install / Enable IIS in Windows WITH CGI</h4>

<p>World Wide Web Services -> Application Development Features -> [X] CGI</p>

<p>
  <img src="https://i.imgur.com/g6HpSAY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/5R6ymoM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/yBBoWMO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)</h4>

<p>
  <img src="https://i.imgur.com/WDjxDNK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/V1yjRwG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)</h4>

<p>
  <img src="https://i.imgur.com/rMM2Qaq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/wGEXOMI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Create the directory C:\PHP</h4>

<p>
  <img src="https://i.imgur.com/oHotiwn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder</h4>

<p>
  <img src="https://i.imgur.com/Zl7qlk1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.)</h4>

<p>
  <img src="https://i.imgur.com/9cW8wDr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/ay2Myqs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)</h4>

- Typical Setup ->
- Launch Configuration Wizard (after install) ->
- Standard Configuration ->
- Username: root
- Password: root

<p>
  <img src="https://i.imgur.com/sHO2H90.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/lEeC6Zd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/XviEkbk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/cNp97Uh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/7c6yBeK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/8rqXXK2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Open IIS as an Admin</h4>

<p>
  <img src="https://i.imgur.com/OBKf0Kl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)</h4>

<p>
  <img src="https://i.imgur.com/xVs1BGG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/8XCMgzA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/ORdSaUR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/urmSaMf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Reload IIS (Open IIS, Stop and Start the server)</h4>

<p>
  <img src="https://i.imgur.com/kLp12g1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Install osTicket v1.15.8</h4>

- From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
- Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
<p>
  <img src="https://i.imgur.com/gCaHCUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/CgkT0Oy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/ME9MJuz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Reload IIS (Open IIS, Stop and Start the server)</h4>

<p>
  <img src="https://i.imgur.com/QDebtWm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Go to sites -> Default -> osTicket</h4>

- On the right, click “Browse *:80”

<p>
  <img src="https://i.imgur.com/apa6HLJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/0OYzC8P.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Enable the disabled Extensions</h4>

- Go back to IIS, sites -> Default -> osTicket
- Double-click PHP Manager
- Click “Enable or disable an extension”
  - Enable: php_imap.dll
  - Enable: php_intl.dll
  - Enable: php_opcache.dll
- Refresh the osTicket site in your browser, observe the changes

<p>
  <img src="https://i.imgur.com/8wVjJK2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/uwihBne.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/rR17FAM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/DPSwz0b.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Rename: ost-config.php</h4>

- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

<p>
  <img src="https://i.imgur.com/W7l0XGk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/NTKGGLI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Assign Permissions: ost-config.php</h4>

- Disable inheritance -> Remove All
- New Permissions -> Everyone -> All

<p>
  <img src="https://i.imgur.com/jfSKEZM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/lcWBb3G.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/xYHoYlJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/EJebAEe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/q53vZyw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/pDxSQMv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Continue Setting up osTicket in the browser (click Continue)</h4>

- Name Helpdesk
- Default email (receives email from customers)

<p>
  <img src="https://i.imgur.com/mKIv3Yk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>From the “osTicket-Installation-Files” folder, install HeidiSQL.</h4>

- Open Heidi SQL
- Create a new session, root/root
- Connect to the session
- Create a database called “osTicket”

<p>
  <img src="https://i.imgur.com/J0gMoVh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/3EitDwu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/RqTzJBb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/RqTzJBb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/OIGs3Vx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/EcOx0ww.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Continue Setting up osTicket in the browser</h4>

- MySQL Database: osTicket
- MySQL Username: root
- MySQL Password: root
- Click “Install Now!”

<p>
  <img src="https://i.imgur.com/TNGYxeN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/7bMdzBy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Congratulations, hopefully it is installed with no errors!</h4>

- Browse to your help desk login page: http://localhost/osTicket/scp/login.php

<p>
  <img src="https://i.imgur.com/0Qcs3DQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/AfEYZr0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>End Users osTicket URL:</h4>

- [http://localhost/osTicket/ ](http://localhost/osTicket/)
<p>
  <img src="https://i.imgur.com/elMq0b1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Clean up</h4>

- Delete: C:\inetpub\wwwroot\osTicket\setup
- Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php

<p>
  <img src="https://i.imgur.com/1qEZ74P.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/hX5TzF6.pngg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />


[<h4>Now continue here</h4>](https://github.com/Dakalo-Ndonde15/post-install-config/)
