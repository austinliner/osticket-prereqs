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

- Enable IIS on windows VM
- Install PHP manager and register with IIS
- Install a web database 
- Create database for osTicket
- Configure permissions and install osTicket

<h2>Deployment and Configuration</h2>

I began by connecting to the virtual machine with remote desktop.
In the virtual machine I opened the control panel and enabled IIS with CGI.
<img width="1440" alt="Enable CGI" src="https://github.com/user-attachments/assets/85dbc29c-61ab-450b-924d-218310455a14">

I went into IIS and registered PHP.
<img width="1440" alt="Register PHP" src="https://github.com/user-attachments/assets/9068d336-0c40-49ec-8c41-2e12a7d5ac0a">

After installing the osTicket files, I enabled the PHP extensions that were not enabled when i opened osTicket for the first time.
<img width="1440" alt="Enable Extensions" src="https://github.com/user-attachments/assets/cb3e38d9-ad47-411c-92c5-cbd3ad85fd98">

I disabled the inheritence in order to assign permissions to everyone.
<img width="1440" alt="Disable Inheritance" src="https://github.com/user-attachments/assets/bb50c2f8-fb65-415b-9ad7-fbb80ce69f5b">

After installing HeidiSQL, i created a new session and then connected to the session.
<img width="1440" alt="Install Heidi SQL" src="https://github.com/user-attachments/assets/5cd6a433-cd8e-4774-aa68-1055a259a8d5">
<img width="1440" alt="Create Session (Heidi)" src="https://github.com/user-attachments/assets/b0f0380b-ae34-4811-a271-3e02295b659f">
<img width="1440" alt="Open Session" src="https://github.com/user-attachments/assets/4121cbe0-f42a-4e29-8083-34bd705b1608">

I then created a new database for osTicket within HeidiSQL, that would be used when finishing setup for osTicket.
<img width="1440" alt="Create Database " src="https://github.com/user-attachments/assets/c3377d1e-0e12-4e8d-98f5-599c7515903d">
<img width="1440" alt="Input database" src="https://github.com/user-attachments/assets/80c63225-a2d2-4c2a-aa64-f251a63021ca">
<img width="1440" alt="Finished 2" src="https://github.com/user-attachments/assets/1045f553-ceeb-47dd-a284-5b85a63fa215">
