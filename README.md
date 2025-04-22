<p align="center">
    <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

# osTicket - Prerequisites and Installation
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.

## Environments and Technologies Used
- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

## Operating Systems Used 
- Windows 10 (21H2)

## List of Prerequisites 
*(Best to download prior to performing the steps below)*
- MySQL Database
- PHP installer
- HeidiSQL
- osTicket installer
- PHP Manager for IIS
- Microsoft Visual C++ Redistributable
- URL Rewrite Module

## Installation Steps

1. **Enable IIS (Internet Information Services)**:
   - Go to **Control Panel** → **Programs and Features** → Click **Uninstall a program**.
   - On the left, click **Turn Windows features on or off**.
   - Check the box for **Internet Information Services** and expand it. 
     - Expand **World Wide Web Services** → **Application Development Features**, and check **CGI**.
   
   ![Enable IIS](https://imgur.com/xJNztgn.png)

2. **Install PHP Manager and the Rewrite Module**:
   - Create a directory: `C:\PHP`.
   - Unzip the PHP Manager into the `C:\PHP` folder.
   - Install Microsoft Visual C++ Redistributable.
   
   ![PHP Manager Installation](https://imgur.com/gKtChVi.png)

3. **Install MySQL Database**:
   - Choose 'Typical' for the setup type during installation.
   - Ensure to check the box to launch the MySQL configuration wizard, and select 'Typical Configuration'.
   - When prompted for security options, type 'root' for the password (not best practice for real-world use, but simplified for this demo).
   
   ![MySQL Installation](https://imgur.com/yyhHq2h.png)

4. **Register PHP within IIS**:
   - Open IIS by right-clicking the Start menu and selecting **Run as Administrator**.
   - Open the PHP Manager, click **Register a new PHP version** and browse to the PHP executable in the C: drive.
   - After clicking **OK**, stop and restart the web server via the IIS Manager.

   ![Register PHP](https://imgur.com/skyrpuZ.png)

5. **Install osTicket**:
   - Unzip the osTicket zip folder and copy the 'upload' folder to `C:\inetpub\wwwroot`.
   - Rename the copied folder to 'osTicket'.
   - Restart the server. In IIS Manager, navigate to **Sites** → **Default Web Site** → click on 'osTicket' → Click on **Browse 80**.
   - Enable the required PHP extensions: `php_imap.dll`, `php_intl.dll`, and `php_opcache.dll` by going to **Sites** → **Default Web Site** → **osTicket** → click on **PHP Manager**.

   ![osTicket Install](https://imgur.com/QuQvAx0.png)

6. **Configure osTicket**:
   - Rename `ost-sampleconfig.php` to `ost-config.php` in `C:\inetpub\wwwroot\osTicket\include`.
   - Set permissions on this file:
     - Right-click the file → **Properties** → **Security** → **Advanced** → **Disable inheritance**, and remove all inherited permissions.
     - Click **Add** → **Select a Principal**. Type `Everyone` and set **Full Control** permissions.

   ![Set Permissions](https://imgur.com/hqDOf2w.png)
   ![Permissions Window](https://imgur.com/u2G4nbQ.png)

7. **Complete osTicket Installation**:
   - In your browser, click **Continue** and provide a help desk name and default email. Set up your primary administrator account credentials.

   ![osTicket Setup](https://imgur.com/xo5ksCT.png)

8. **Installing HeidiSQL**:
   - After installation, launch HeidiSQL and click **New**.
   - Set both user and password to `root`, and then click **Open**.
   - Right-click on 'Unnamed' and select **Create New** → **Database**. The database name will be `osTicket`.

   ![HeidiSQL Database Setup](https://imgur.com/xo5ksCT.png)

9. **Finalizing osTicket Installation**:
  - Return to your browser to continue with the osTicket installation.
  - Under **Database Settings**, enter the following:
  - **Database**: osTicket
  - **Username**: root
  - **Password**: root

- Click **Install**. You are now ready to use osTicket!

![Final Step of Installation](https://imgur.com/fdc6NGZ.png)
