#Overview: Lab 4 Windows 10, Join PC to Domain
<p>
This section of my home lab documentation demonstrates the process of creating a windows 10 Pro VM and joining the to a domain we created "junicetechie.com" and managing server roles through Server Manager. The project covers the steps for configuring a Windows 10 PC to be part of an Active Directory domain, and leveraging Server Manager to manage server roles and features within the domain.
</p>
<p>
#Objectives
Create another VM and install Windows 10 on the PC.  
Join a Windows 10 PC to our domain.
Use Server Manager to manage server roles and features in a domain environment.
Perform basic administrative tasks such as user management and role configuration from a client machine using RSAT.
</p>
</br>
#Documentation
<p>
In this home lab, I will demonstrate how to install Windows 10 and join it to our domain (junicetechie.com). To achieve this, we will create a separate virtual machine for the Windows 10 installation. The process begins with downloading the Windows 10 Installation Media Tool from the official Microsoft website:https://www.microsoft.com/en-us/software-download/windows10.
</p>
Open the media tool installer and click 'Accept.' Next, select 'Create installation media (USB flash drive, DVD, or ISO file) for another PC.' Save the download to your 'Downloads' folder, and you should be able to access it from the VirtualBox.
<p>
1. <p align="center">
   <img src="https://github.com/Eunice-Kamore/Installing-VirtualBox-and-Windows-Server-2022/blob/9200c774c0a6c5e371306e49e2755f3be7c9a306/Files/Edited%20one.PNG" width="400px"/>
   <br />
   <br />
2. <p align="center">
   <img src="https://github.com/Eunice-Kamore/Installing-VirtualBox-and-Windows-Server-2022/blob/9200c774c0a6c5e371306e49e2755f3be7c9a306/Files/Edited%20one.PNG" width="400px"/>
   <br />
   <br />
Next, open your VirtualBox and create a new virtual machine. Click Machine in the top-left corner, then select New.  
3. <p align="center">
   <img src="https://github.com/Eunice-Kamore/Installing-VirtualBox-and-Windows-Server-2022/blob/9200c774c0a6c5e371306e49e2755f3be7c9a306/Files/Edited%20one.PNG" width="400px"/>
   <br />
   <br />
Name the virtual machine "Windows 10 (Helpdesk)" For the ISO image, navigate to the Downloads folder, click the dropdown icon, select "Other," and choose the "Windows.ISO" file. Follow the steps that we went through to create the server 2022 VM.

After creating the VM click on "Start" to boot the machine and begin the installation. The setup screen will appear. Click ""Next after selecting your language and on the next page click on "Install Now".
4. <p align="center">
   <img src="https://github.com/Eunice-Kamore/Installing-VirtualBox-and-Windows-Server-2022/blob/main/Files/Downloading%20server%202022.png?raw=true" width="400px"/>
   <br />
   <br />
5. <p align="center">
   <img src="https://github.com/Eunice-Kamore/Installing-VirtualBox-and-Windows-Server-2022/blob/main/Files/Downloading%20server%202022.png?raw=true" width="400px"/>
   <br />
   <br />

On the next page, select "I don't have a product key" and click next. 

6. <p align="center">
   <img src="https://github.com/Eunice-Kamore/Installing-VirtualBox-and-Windows-Server-2022/blob/main/Files/Downloading%20server%202022.png?raw=true" width="400px"/>
   <br />
   <br />
Then on the next page, make sure to select "Windows 10 Pro", click "Next" and check the box to accept terms and conditions.

7. <p align="center">
   <img src="https://github.com/Eunice-Kamore/Installing-VirtualBox-and-Windows-Server-2022/blob/main/Files/Downloading%20server%202022.png?raw=true" width="400px"/>
   <br />
   <br />

8. <p align="center">
   <img src="https://github.com/Eunice-Kamore/Installing-VirtualBox-and-Windows-Server-2022/blob/main/Files/Downloading%20server%202022.png?raw=true" width="400px"/>
   <br />
   <br />

Select "Custom: Install Windows only," then click Next to begin the installation of Windows 10.

9. <p align="center">
   <img src="https://github.com/Eunice-Kamore/Installing-VirtualBox-and-Windows-Server-2022/blob/main/Files/Downloading%20server%202022.png?raw=true" width="400px"/>
   <br />
   <br />
Once the installation is finished, this page will appear. We will now begin the setting up the local account on this PC.

10. <p align="center">
   <img src="https://github.com/Eunice-Kamore/Installing-VirtualBox-and-Windows-Server-2022/blob/main/Files/Downloading%20server%202022.png?raw=true" width="400px"/>
   <br />
   <br />

Choose your preferred region and then 



















