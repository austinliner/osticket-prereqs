# osticket-prereqs
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

- Enable IIS on Windows VM
- Install PHP manager and register with IIS
- Install a web database 
- Create a database for osTicket
- Configure permissions and install osTicket

<h2>Deployment and Configuration</h2>

Begin with creating a virtual machine within Microsoft Azure.
<img width="1258" alt="Screenshot 2024-09-19 at 3 48 39 PM" src="https://github.com/user-attachments/assets/eff6d795-7ea9-4bac-b0dc-4f566aeaeb78">

Find the public IP address of your virtual machine and connect to it with remote desktop.
<img width="1258" alt="Screenshot 2024-09-19 at 3 58 48 PM" src="https://github.com/user-attachments/assets/9536bcbf-b1d8-4aab-a6c0-85653aa28942">
<img width="711" alt="Screenshot 2024-09-19 at 3 59 12 PM" src="https://github.com/user-attachments/assets/aeec068b-2b0e-4abe-ab1d-8262248d2e1d">

Copy the osticket installation folder onto your virtual machine desktop.
<img width="1440" alt="Screenshot 2024-09-19 at 4 04 04 PM" src="https://github.com/user-attachments/assets/c45a4f80-7d58-4455-96ea-9575945dd6e5">

Enable IIS with CGI by going to Control Panel> Uninstall Programs> Turn Windows features on or off. Check all boxes under Internet Information Services. Go to the World Wide Web Services> Application Development Features and check the box for CGI.
<img width="1440" alt="Screenshot 2024-09-19 at 4 05 53 PM" src="https://github.com/user-attachments/assets/2af155c2-35e5-4d07-ab6e-2ffe4b43d33f">
<img width="1440" alt="Screenshot 2024-09-19 at 4 07 46 PM" src="https://github.com/user-attachments/assets/85cb1ed5-3d98-446d-aa2c-1aecd19caf9b">

Begin installing the files from the osticket folder, with PHP manager for IIS and the Rewrite Module.
<img width="843" alt="Screenshot 2024-09-19 at 4 26 37 PM" src="https://github.com/user-attachments/assets/b022b2c3-0e7e-4d52-a343-e860703ed809">

Create a new folder in the C: drive named "PHP" 
<img width="843" alt="Screenshot 2024-09-19 at 4 29 23 PM" src="https://github.com/user-attachments/assets/6352345f-50e3-410a-9042-008e2d8eaeaa">

Unzip the files from PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the PHP folder we just created. (Right-click> extract all> browse for the PHP folder in the C: drive.
<img width="843" alt="Screenshot 2024-09-19 at 4 31 44 PM" src="https://github.com/user-attachments/assets/b640c6ed-a525-4ad0-85bf-d09d6e4c09c4">
<img width="843" alt="Screenshot 2024-09-19 at 4 32 21 PM" src="https://github.com/user-attachments/assets/c2758a6d-d617-4e10-81c7-de83a08bb0d2">

Continue installing files from the osticket folder with VC_redist.x86.exe.
<img width="843" alt="Screenshot 2024-09-19 at 4 38 24 PM" src="https://github.com/user-attachments/assets/879cb689-c75e-4b3b-ae94-c92b1f5aac98">


From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
Typical Setup ->
Launch Configuration Wizard (after install) ->
Standard Configuration ->
Username: root
Password: root
<img width="843" alt="Screenshot 2024-09-19 at 4 40 05 PM" src="https://github.com/user-attachments/assets/7ecc8643-5746-4af1-85e9-94b00ec70aa5">
<img width="843" alt="Screenshot 2024-09-19 at 4 40 31 PM" src="https://github.com/user-attachments/assets/9703a2cd-5965-4eab-ace0-685f343fa52e">

Run IIS as an administrator 
<img width="843" alt="Screenshot 2024-09-19 at 4 43 45 PM" src="https://github.com/user-attachments/assets/4787a158-e82c-4c10-a873-96d5fd76bf50">

Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)
<img width="914" alt="Screenshot 2024-09-19 at 4 46 06 PM" src="https://github.com/user-attachments/assets/36a8060b-c51c-472b-b392-7eea674200f6">
<img width="914" alt="Screenshot 2024-09-19 at 4 49 19 PM" src="https://github.com/user-attachments/assets/0cb42be0-3ec8-4e2c-80ea-a3370de82336">
<img width="914" alt="Screenshot 2024-09-19 at 4 47 03 PM" src="https://github.com/user-attachments/assets/4849a4b1-8665-46ae-b761-95dae408c29b">
<img width="914" alt="Screenshot 2024-09-19 at 4 47 26 PM" src="https://github.com/user-attachments/assets/902db038-40db-4872-8f5b-7755655c5516">

From the home page in IIS, restart IIS. 
<img width="914" alt="Screenshot 2024-09-19 at 4 47 51 PM" src="https://github.com/user-attachments/assets/9cc00e46-e046-4e8b-8179-85429e8ff68e">

Extract all files from the osTicket v1.15.8. folder and copy the “upload” folder into “c:\inetpub\wwwroot”
<img width="914" alt="Screenshot 2024-09-19 at 5 06 02 PM" src="https://github.com/user-attachments/assets/1113fa45-0106-4b7a-873e-1e6ad52dd7df">
<img width="914" alt="Screenshot 2024-09-19 at 5 01 07 PM" src="https://github.com/user-attachments/assets/9aaba509-f396-4b06-89dc-d135bb2ea5a6">
<img width="914" alt="Screenshot 2024-09-19 at 5 02 18 PM" src="https://github.com/user-attachments/assets/4ef80cc5-d699-4410-b9ff-f3159ddfaf3f">
<img width="914" alt="Screenshot 2024-09-19 at 5 02 25 PM" src="https://github.com/user-attachments/assets/795aa6c9-7f53-40d8-be61-b2ff50020212">

Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
<img width="914" alt="Screenshot 2024-09-19 at 5 02 52 PM" src="https://github.com/user-attachments/assets/d3714e73-c14e-4ecb-874b-71021278469e">
<img width="896" alt="Screenshot 2024-09-19 at 5 11 34 PM" src="https://github.com/user-attachments/assets/ea3b057c-f40d-40ac-9e8c-cfc4e6f3c36e">

Reload IIS (Open IIS, Stop and Start the server)
Go to sites -> Default -> osTicket
On the right, click “Browse *:80”
<img width="920" alt="Screenshot 2024-09-19 at 5 15 51 PM" src="https://github.com/user-attachments/assets/7fc36286-3b0a-4b63-beea-ea66976d1c3c">
<img width="1016" alt="Screenshot 2024-09-19 at 5 16 23 PM" src="https://github.com/user-attachments/assets/c7b8fa2e-9a0f-4555-ba0e-49bce41c854c">

Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
<img width="1016" alt="Screenshot 2024-09-19 at 5 19 04 PM" src="https://github.com/user-attachments/assets/0bb416d1-aeeb-49c8-b965-4170c670142e">

Click “Enable or disable an extension”
<img width="1016" alt="Screenshot 2024-09-19 at 5 19 12 PM" src="https://github.com/user-attachments/assets/dcd47aa5-2652-4379-9fb5-95d3e293e7af">

Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
<img width="921" alt="Screenshot 2024-09-19 at 5 19 40 PM" src="https://github.com/user-attachments/assets/ce7b22b7-cd9f-4ff6-a3b8-1cd6990b77f1">
<img width="921" alt="Screenshot 2024-09-19 at 5 20 05 PM" src="https://github.com/user-attachments/assets/2483c604-560a-4656-8c1f-e8ff3b7188ec">

Go back to the osTicket site refresh, and notice the changes.
<img width="1026" alt="Screenshot 2024-09-19 at 5 22 46 PM" src="https://github.com/user-attachments/assets/07925e01-df87-42a6-b10f-fd7e5200b734">

Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

<img width="821" alt="Screenshot 2024-09-19 at 5 26 18 PM" src="https://github.com/user-attachments/assets/e917879b-5e03-4853-a338-e6caeee6ad85">
<img width="821" alt="Screenshot 2024-09-19 at 5 26 43 PM" src="https://github.com/user-attachments/assets/00b166a5-b475-4a08-9090-2b2ae836aacc">
<img width="821" alt="Screenshot 2024-09-19 at 5 26 55 PM" src="https://github.com/user-attachments/assets/66bfbc84-ef44-447c-990a-3807e1646b40">

Assign Permissions: ost-config.php.
Right-click the ost-config.php folder and go to properties.
<img width="821" alt="Screenshot 2024-09-19 at 5 29 38 PM" src="https://github.com/user-attachments/assets/82e9ba39-6abe-432b-9662-151604614c8a">

Go to the Security tab> Advanced
<img width="374" alt="Screenshot 2024-09-19 at 5 30 49 PM" src="https://github.com/user-attachments/assets/5afc7e25-ce39-477d-8784-305d887582bb">

Disable inheritance -> Remove All
<img width="766" alt="Screenshot 2024-09-19 at 5 31 07 PM" src="https://github.com/user-attachments/assets/a9db4549-3b44-454f-a2ae-7d422a206daa">
<img width="766" alt="Screenshot 2024-09-19 at 5 31 44 PM" src="https://github.com/user-attachments/assets/4d40987a-feb4-4405-bf67-e18e4f29569d">

New Permissions -> Everyone -> All
<img width="766" alt="Screenshot 2024-09-19 at 5 32 27 PM" src="https://github.com/user-attachments/assets/dd9e0420-1a5d-43c1-a186-00cabbda1ccb">

Continue setting up osTicket in the browser.
<img width="868" alt="Screenshot 2024-09-19 at 5 39 12 PM" src="https://github.com/user-attachments/assets/14f00ffa-a522-4521-a57d-2b12e4906a9e">

From the “osTicket-Installation-Files” folder, install HeidiSQL.
<img width="831" alt="Screenshot 2024-09-19 at 5 40 52 PM" src="https://github.com/user-attachments/assets/6fadfa4d-3cba-4863-9d87-93571773df4f">

Open HeidiSQL and create a new session. username: root  password: root and connect to the session.
<img width="727" alt="Screenshot 2024-09-19 at 5 41 59 PM" src="https://github.com/user-attachments/assets/e8971b28-52b7-4b2a-aeb9-123c1a403a60">
<img width="727" alt="Screenshot 2024-09-19 at 5 42 18 PM" src="https://github.com/user-attachments/assets/593b85a0-17a2-41df-a1d7-4504352609ad">
<img width="934" alt="Screenshot 2024-09-19 at 5 42 39 PM" src="https://github.com/user-attachments/assets/7c96b532-fadf-493f-a901-0e0842b85685">

Create a new database named osTicket.
<img width="934" alt="Screenshot 2024-09-19 at 5 43 18 PM" src="https://github.com/user-attachments/assets/45a174d2-5bfd-41d3-b4cd-5365d0812789">
<img width="934" alt="Screenshot 2024-09-19 at 5 43 33 PM" src="https://github.com/user-attachments/assets/9a3c8ee4-abb0-43a2-9002-61d103da7862">
<img width="934" alt="Screenshot 2024-09-19 at 5 43 48 PM" src="https://github.com/user-attachments/assets/466cdb08-ced7-40bb-b45d-d4cd74b68987">

Continue setting up osTicket in the browser. Input the database we just created, "osTicket" using the same username and password: root
<img width="869" alt="Screenshot 2024-09-19 at 5 51 00 PM" src="https://github.com/user-attachments/assets/f433a27b-7cd5-4f92-af43-d5c3fe284030">
<img width="869" alt="Screenshot 2024-09-19 at 5 52 33 PM" src="https://github.com/user-attachments/assets/45b9c72e-2a7a-46f6-b4ca-d589ba836640">


