<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- https://www.loom.com/share/Setting-up-OS-Ticket-on-Windows-10-dacb463f955047d89789f5dc8e70c527?sid=f667fc0b-2908-4233-93e5-db8809bfc376

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- Internet Information Services (IIS)
- PHP Manager
- Rewrite Module
- VC Redist
- MySQL
- Heidi SQL
- osTicket v1.15.8
- Link to downloads: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

<h2>Installation Steps</h2>

<p>
1. First, you want to go to portal.azure.com. Once there, we need to create a resource group and a Windows Virtual Machine. We need to make sure the image we choose is Windows 10. Once that is done, it will create a Virtual Network (Vnet)
</p>
2. Next, we need to log into the virtual machine using the public ip address of VM-1.
<p>
<img width="1150" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/16aa8d77-668b-4413-9bf4-8e4124557e8a">
<p>
3. Now that we are logged intp the virtual machine, we need to instll/enable IIS with CGI and Common HTTP Features and the IIS Management Console. In order to do that, go to settings, programs and features, then "click turn Windows Features on or off". CLick Internet Information Services -> Web Management Tools -> Make sure IIS Management Console is selected. Then, Click World Wide Web Services -> Application Development Features -> Make sure CGI is selected -> CLick Common HTTP Features and ensure all boxes are checked. Press okay and the system should make the changes. 
<p>
<img width="946" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/79073f6e-2660-49e9-bfdd-0878015e0fd4">
<p>
<img width="1035" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/9438945d-44f6-417b-a321-6b6ed33917fa">
<p>
<img width="357" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/e6d9a3e4-4a00-4558-b7d0-2c455dae9982">
<p>
<img width="362" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/2fb1e846-98c7-4fa4-abde-8f6d8057c240">
<p>
<img width="403" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/dc329b16-4e27-416a-b482-c7dd1fa44dd0">
<p>
<img width="408" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/1be1089a-92db-402b-aec8-fe8d25213ced">
<p>
4. From the installation files, install the PHP Manager for IIS and install the Rewrite Module. Then, in the C:\ Drive, Create a new directory (folder) named PHP (This PC -> C:\ -> Right Click and Create New Folder)
</p>
<img width="495" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/2c7e8b34-f2c9-40d6-a416-5a017703170a">
<p>
<img width="492" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/daa892c7-e76b-4538-9b7a-622a14c6bb4a">
<p>
<img width="594" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/ed2fd3d5-aa26-4438-b038-5178c7ff4fbf">
<p>
5. Now we need to download PHP.7.3.8 and extract it into the PHP Directory we previously created, download and install VC Redist (C++), and download and install MySQL (Typical Setup, Standard Configuration)
<p>
<img width="610" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/f81c1a35-171b-46f1-b92c-eeacdac06e69">
<p>
<img width="475" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/2151c932-49e3-4e43-a3a9-11d0167e3ab3">
<p>
6. Now we need to click on start, type IIS and right click it and run it as an administrator. Once the window comes up, click VM-1 in the left panel -> Sites -> Default Websites and click PHP manager. Now, click register and when it asks for a path, click the PHP folder and the php-cgi file. Finally, we can go back to where we started by clicking VM-1 in the left corner and resloading the IIS pressing stop then start to the right.
</p>
<img width="990" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/aef259a8-fd94-49eb-b1d5-02822bd18fcf">
<img width="746" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/85711de5-68a6-4afc-9566-cd3dc3150792">
<img width="205" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/fd942cb5-8cec-403e-b0b6-3e5323ea2ee2">
</p>
7. Now we can install osTicket. To do that, we need to download osTicket v1.15.8. Once we download it, there is a folder called "upload" in the files. we need to drag that folder to C:\ -> inetpub -> wwwwroot. Dragging the folder here will automatically extract it. Once it is done, rename  the "upload" to "osTicket" (make sure to name this exactly as spelled ot you will run into some issues)
<img width="1244" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/53844897-50d2-4fe7-a134-08a394fa07f1">
<p>
8. Now, we should be able to tell if the installation worked. To do that, we need to reload IIS. Remember to run it as an administrator. Once it is open, we need to stop and start the server again. Once we do that go to sites -> Default -> osTicket. On the right, click "Browse *.80". If you did it correctly, the osTicket website should pop up.
<img width="985" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/621417b5-1878-4950-8934-8fe5ca80b76a">
<img width="1365" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/91115f62-09ad-45d8-9873-dfa5449f43e5">
9. Next, we need to enable some extensions that are not enabled. We can do this by going to IIS site -> Default -> osTicket. Click the PHP Manager then click "enable or disable an extension". Enable the following: php_imap.dll; php_intl.dll; php_opcache.dll. Refresh osTicket in the browser to make sure those are enabled.
<img width="777" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/f8b5a7c5-a49e-40b0-abb6-33b6fdd4d05e">
<img width="839" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/d4b2ffa6-df97-4b7c-8c29-35c3afc2fb3c">
<p>
10. We need to rename ost-sampleconfig.php. We can find it at C:\-> inetpub -> wwwwroot -> osTicket -> include. Rename it to ost-config.php
<p>
<img width="627" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/7b7e425c-4622-484e-b68b-9310fb08e3f0">
<img width="718" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/f0744c3d-65ab-485c-87de-0e2c27da943b">
<p>
11. We need to assign permissions to the file that we just renamed. Right click -> Properties -> Advanced -> Disable Inheritance -> Remove All. Then click Add principal -> type everyone and check names -> check all boxes -> apply
12. Continue setting up osTicket in the browser by clicking continue. 
Name Helpdesk and set up a default email
<img width="794" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/ff4282a4-5dfe-4de1-b62f-f4e9fc019b91">
<p>
13. Before we can go further, we need to install a database by downloading and installing HeidiSQL. Open HeidiSQL and create a new session. Connect to the session, create a database called osTicket. We can continue setting up osTicket in the browser. Once we enter the required information, click "Install Now". If we got no errors, we finally have osTicket installed.
<img width="592" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/cdeb6f34-bd4a-4f6a-b5ac-b64961c805f3">
<img width="621" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/6a80d17d-419f-4b0e-83cd-4fdb6dbda0ee">
<img width="821" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/55f0789d-7cab-4e5a-9cfa-1a13e0d192c5">
</p>
14. Finally, we need to clean up some files and set permissions. Delete the setup folder. You can find it C:\ -> inetpub -> wwwroot -> osTicket -> Delete entire setup folder. Go into osTicket -> include -> right click ost-config.php and change permissions to "Read" only
Browse to your help desk login page: http://localhost/osTicket/scp/login.php  
End Users osTicket URL: http://localhost/osTicket/ 
<img width="904" alt="image" src="https://github.com/JavariusFields/osticket-prereqs/assets/144845191/87a4fe1a-73d6-4f78-970f-c062957738d4">

