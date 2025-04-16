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
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
