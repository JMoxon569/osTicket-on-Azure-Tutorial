﻿**Install osTicket on Azure VM**

**Introduction**

This guide provides step-by-step instructions on how to install osTicket, a popular open-source ticketing system, on a virtual machine hosted in Microsoft Azure. We will start by setting up a new virtual machine and then proceed to install and configure osTicket.

**Prerequisites**

- An active Microsoft Azure account.
- Basic familiarity with Azure services, especially Virtual Machines.
- Access to SSH or RDP tools, depending on the operating system you choose.

**Steps to Install osTicket**

**Step 1: Create and Configure Your Azure Virtual Machine**

**1.1 Log in to the Azure Portal**

- Navigate to the Azure Portal and sign in with your credentials.

**1.2 Create a New Virtual Machine**

- Go to Virtual machines in the sidebar and click on + Create.
- Choose your desired OS (Ubuntu Server 20.04 LTS for Linux setups, or Windows Server for Windows setups).
- Fill in the details such as VM name, region, availability options, and size. A B1s size is sufficient for demonstration purposes but consider a more robust size for production.
- Set up authentication type (recommend SSH keys for Linux, Username and password for Windows).
- Configure networking settings to ensure the VM can be accessed over the internet.
- Click Review + create once all configurations are set, then click Create.

**1.3 Access the VM**

- Once the VM is deployed, go to the resource and note down the public IP address.
- Connect to your VM using SSH (Linux) or Remote Desktop (Windows).

**Step 2: Install osTicket**

**For Windows:**

**2.1 Install XAMPP or WAMP**

- Install XAMPP or WAMP to manage Apache, MySQL, and PHP. These tools provide an all-in-one server solution that includes all the necessary components to run osTicket.

**2.2 Download osTicket**

- Navigate to the osTicket official download page and download the latest version of osTicket.
- Upload the download package to your VM and extract it to your web server's root directory (e.g., C:\xampp\htdocs for XAMPP).

**2.3 Configure the Database**

- Open the XAMPP Control Panel and start the MySQL service.
- Access phpMyAdmin from the XAMPP Control Panel or by visiting http://localhost/phpmyadmin in your web browser.
- Log in to your MySQL database using the command: mysql -u root -p
- Create a new database for osTicket using the command: CREATE DATABASE osticket;
- Grant all privileges on osticket to 'osticketuser'@'localhost' identified by 'YourPasswordHere' using the command: GRANT ALL PRIVILEGES ON osticket.\* TO 'osticketuser'@'localhost' IDENTIFIED BY 'YourPasswordHere';
- Flush privileges and exit using the commands: FLUSH PRIVILEGES; EXIT;

**2.4 Run the osTicket Installer**

- Open your web browser and go to http://<Your-VM-IP>/setup/.
- Follow the on-screen instructions to configure osTicket. This will involve setting up the database connection with the details you created and configuring primary settings.
- Once installation is complete, remove the setup directory for security using the command: sudo rm -rf /var/www/html/setup/

**Conclusion**

You have successfully installed osTicket on your Azure virtual machine. You can now proceed to configure your ticketing system according to your organization's needs.

