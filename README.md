<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites (Best to download prior to performing steps below)</h2>


- MySQL Database
- PHP installer
- HeidiSQL
- osTicket installer
- PHP Manager for IIS
- Microsoft Visual C++ Redistributable
- URL Rewrite Module

<h2>Installation Steps</h2>


<p>
    First, enable IIS (Internet Information Services) by going to --> <b>Control Panel</b> -->  <b>Programs and Features</b> --> click <b>uninstall a program</b>. To the left of the window, click on <b>Turn windows features on or off</b>. Check the box for <b>Internet Information Services</b> and then expand it. Expand <b>World Wide Web Services</b> then expand it. Expand <b>Application Development Features</b> then check CGI. This will install the web server.
</p>
p>
    <img src="https://imgur.com/xJNztgn.png" style="height: 80%; width: 80%;" alt="Disk Sanitization Steps"/>
</p>
<br/>



<p>
Next, install the PHP Manager and the Rewrite Module. Create a directory on your computer's C drive.
This is the path: C:\PHP. Name that directory PHP. Next, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder.
Then, install the C_redist.x86.exe  and the mysql-5.5.62-win32.msi files. When installing MySQL, choose 'Typical' for the setup type. Make sure the box is checked to launch the MySQL configuration wizard an choose  typical configuration on that window. When the window to modify security option appears type 'root' for the password. (This is not best practice in the real world, it just makes it easier for this demo)


</p>
<p>
<img src="https://imgur.com/gKtChVi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now, go back to IIS  and register PHP within IIS. Go to the Start menu and open IIS by right-clicking and running as an administrator. Open the PHP Manager, click 'register a new PHP version and browse to the PHP executable housed in the C: drive. After clicking 'ok', stop and restart the web server by clicking the osticket vm and then clicking stop. Click it again click start.
</p>
<br />

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now, we are ready to install osTicket. Unzip the osticket zip folder. Copy the 'upload' folder into this path: c:\inetpub\wwwroot. Rename the folder within the path to 'osTicket'. Restart the server again. From within the IIS Manager, go to sites--> Default Web Site--> and click on osTicket. On the right panel click on Browse 80. In the IIS Manager we must enable some dependencies, these include: php_imap.dll, php_intl.dll, and php_opcache.dll. We do this by going to Sites-->Default Web Site--> osTicket---> and clicking on PHP Manager. The disabled extensions are gray. Enable them by right clicking on them and clicking enable.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we need to rename the ost-config php file from C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to C:\inetpub\wwwroot\osTicket\include\ost-config.php. We can now assign permissions on this file which will allow osTicket to make changes to this file. Right-Click on the file, go to Properties--> Security--> Advanced. Click disable inheritance and click 'remove all inherited permissions'. Click Add--> Select a Principal. In the box where you can ente an object name, type 'everyone' (Not best practice for the real-world, but okay for this demo). For Basic Permissions, check: full control. Click 'apply' and 'ok'.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We will continue with the osTicket installation within our browser. Click 'Continue' and provide a help desk name and default email. Then set up your primary administrator account credentials. 
</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Now, we will install HeidiSQL. After installing, you will see the Heidi SQL installation manager. Click 'new'. Make sure your user and password are both set to root. Then click 'open'. The database is now unnamed. Right click on 'unnamed' and click 'create new'--> 'database'. The database will be called 'osTicket'.
</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Back to te browser, continue with the osTicket installation. Under 'Database Settings' type osTicket as the Database, and root as bothe the username and password. Then install. You are now ready to use osTicket!
</p>
<br />
