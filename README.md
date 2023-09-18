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
7.




<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
