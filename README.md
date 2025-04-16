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

<h2>List of Prerequisites</h2>

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
First, enable IIS (Internet Information Services) by going to the Control Panel. Under Program, click 'uninstall a program'. To the left of the window, click on 'Turn windows features on or off'. Check the box for 'Internet Information Services' and then expand it. Expand 'Word Wide Web Services' then expand 'Application Development Features' then check CGI. This will install the web server.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, install the PHP Manager, the Rewrite Module, which is listed in the prerequisites. Create a directory on your computer's C drive.
This is the path: C:\PHP. Name that directory PHP. Next, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder.
Then, install the C_redist.x86.exe  and the mysql-5.5.62-win32.msi files. When installing MySQL, choose 'Typical' for the setup type. Make sure the box is checked to launch the MySQL configuration wizard an choose standard configuration on that window. When the window to modify security option appears type 'root' for the password. (This is not best practice in the real world, it just makes it easier for this demo)


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
