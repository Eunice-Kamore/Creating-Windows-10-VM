<H1>Overview: Lab 4 Windows 10, Join PC to Domain</H1>
<p>
This section of my home lab documentation demonstrates the process of creating a windows 10 Pro VM and joining it to the domain that we created "junicetechie.com" and managing server roles through Server Manager. The project covers the steps for configuring a Windows 10 PC to be part of an Active Directory domain, and leveraging Server Manager to manage server roles and features within the domain.
</p>

<H2>Objectives</H2>

--Create another VM and install Windows 10 on the PC.  

--Join a Windows 10 PC to our domain.

--Use Server Manager to manage server roles and features in a domain environment.

--Perform basic administrative tasks such as user management and role configuration from a client machine using RSAT.


<H2>Documentation</H2>
<p>
In this home lab, I will demonstrate how to install Windows 10 and join it to our domain (junicetechie.com). To achieve this, we will create a separate virtual machine for the Windows 10 installation. The process begins with downloading the Windows 10 Installation Media Tool from the official Microsoft website:https://www.microsoft.com/en-us/software-download/windows10.
</p>
To begin we will navigate to Microsoft Official page and search for Windows 10 Installation Media. Click "Download Now" and the .exe file will be downloaded on your computer. You should find it on the downloads folder. 

1.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/One.PNG?raw=true"  height="80%" width="80%"/>
   <br />
   <br />
2.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Two.PNG?raw=true"  height="80%" width="80%"/>
   <br />
   <br />

Open the media tool installer and click 'Accept.' Next, select 'Create installation media (USB flash drive, DVD, or ISO file) for another PC.' Save the download to your 'Downloads' folder, and you should be able to access it from the VirtualBox.


3.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Three.PNG?raw=true"  height="80%" width="80%"/>
   <br />
   <br />
   
Click "Next"

4. <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Four.png?raw=true"  height="80%" width="80%"/>
   <br />
   <br />
   
Select "ISO File" and Click "Next" and the download should begin. The ISO File is saved on the Downloads folder.

5.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Five.png?raw=true"  height="80%" width="80%"/>
   <br />
   <br />   
   
Next, open your VirtualBox and create a new virtual machine. Click Machine in the top-left corner, then select New. Then name the virtual machine "Windows 10 (Helpdesk)" For the ISO image, navigate to the Downloads folder, click the dropdown icon, select "Other," and choose the "Windows.ISO" file. Follow the steps that we went through to create the server 2022 VM.  

6.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Six.PNG?raw=true"  height="80%" width="80%"/>
   <br />
   <br />

Once the VM is created and the ISO File mounted, we can proceed with installation. Click "Start" to boot the machine and begin the installation. The setup screen will appear. Click "Next" after selecting your language and on the next page click on "Install Now".


7.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Seven.png?raw=true"  height="80%" width="80%"/>
   <br />
   <br />
   
8.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Eight.png?raw=true"  height="80%" width="80%"/>
   <br />
   <br />

On the next page, select "I don't have a product key" and click next. 


9.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Nine.PNG?raw=true"  height="80%" width="80%"/>
   <br />
   <br />
   
Then on the next page, make sure to select "Windows 10 Pro", click "Next" and check the box to accept terms and conditions.




10.<p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Ten.png?raw=true"  height="80%" width="80%"/>
   <br />
   <br />

11.<p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Eleven.PNG?raw=true"  height="80%" width="80%"/>
   <br />
   <br />

Select "Custom: Install Windows only," then click Next to begin the installation of Windows 10.

12.

   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Twelve.PNG?raw=true"  height="80%" width="80%"/>
   <br />
   <br />

Choose the disk and click "Next" and wait for the installation to complete.

13.
  
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Thirteen.png?raw=true"  height="80%" width="80%"/>
   <br />
   <br />
   
14.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Fourteen.png?raw=true"  height="80%" width="80%"/>
   <br />
   <br />

Once the installation is finished, this page will appear. We will now begin the setting up the local account on this PC.
Choose your preferred region and click "Next"


15.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Fifteen.png?raw=true"  height="80%" width="80%"/>
   <br />
   <br />
   
Choose your preferred keyboard layout as well and click "Next". On the next page click "Skip"

16.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Sixteen.png?raw=true" height="80%" width="80%"/>
   <br />
   <br />
   
17.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Seventeen.png?raw=true"  height="80%" width="80%"/>
   <br />
   <br />

Select "Set up for personal use"

18.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Eighteen.PNG?raw=true"  height="80%" width="80%"/>
   <br />
   <br />

   
Choose "Offline Account"


19.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Nineteen.PNG?raw=true"  height="80%" width="80%"/>
   <br />
   <br />

Choose the "Limited Experience" option.

20.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Twenty.PNG?raw=true"  height="80%" width="80%"/>
   <br />
   <br />
   
Input the name of your choice. For this lab I have chosen "Local User". Then input your password and confirm the same on the next page.

21.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Twenty%20One.png?raw=true" height="80%" width="80%"/>
   <br />
   <br />
   
22.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Twenty%20Two.png?raw=true"  height="80%" width="80%"/>
   <br />
   <br />
   
Select and answer any three security questions of your choice and click next.

23.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Twenty%20Three.png?raw=true"  height="80%" width="80%"/>
   <br />
   <br />

Turn off all the additional features to prevent too much CPU and Memory usage for our VM.


24.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/TwentyFour.png?raw=true"  height="80%" width="80%"/>
   <br />
   <br />
   
Click "Skip" 

25.  
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/TwentyFive.png?raw=true"  height="80%" width="80%"/>
   <br />
   <br />
      
Choose "Not Now"

      
26.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/TwentySix.PNG?raw=true"  height="80%" width="80%"/>
   <br />
   <br />

   
The set up is done and the Windows 10 PC is all set.

27.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/TwentySeven.png?raw=true"  height="80%" width="80%"/>
   <br />
   <br />

Now we have our windows PC setup, we'll go ahead and join it to the domain "junicetechie.com". The first step is to assign a static IP Address (10.0.2.16) to our client machine and use the IP Address of the domain controller (10.0.2.15) as the DNS server. 

28.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Twenty8.PNG?raw=true"  height="80%" width="80%"/>
   <br />
   <br />

Secondly, we will create a NAT Network and ensure both the client machine and the Domain Controller are attached to it to enable communication between them. To do this, open the "Tools" then "Network" and cross over to "NAT Networks" and click on "Create" at the top to create a new NAT Network and name it "Homelab" and click "Apply".

29.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Twenty9.PNG?raw=true"  height="80%" width="80%"/>
   <br />
   <br />

Next, we are going to attach both of the VMs to this network. Click on a VM and then go to "Settings" and choose "Network". Then, on the "Adapter 1", and on "Attached to:" open the drop-down and choose "NAT Network". Then choose the Name of the NAT Network we created "Home Lab" and click "OK"   
30.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Thirty.PNG?raw=true"  height="80%" width="80%"/>
   <br />
   <br />  

31.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Thirty1.PNG?raw=true"  height="80%" width="80%"/>
   <br />
   <br /> 
Now, our VMs are on the same network and they can communicate successfully. We"ll go ahead and join the Client to the domain. Open "Settings" on the computer and choose "Accounts".
Then open "Access work or school" and click "Connect".


32.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Thirty2.PNG?raw=true"  height="80%" width="80%"/>
   <br />
   <br /> 

33.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Thrity3.PNG?raw=true"  height="80%" width="80%"/>
   <br />
   <br /> 

Choose to join the option to join the device to a local Active Directory Domain.


34.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Thrity4.PNG?raw=true"  height="80%" width="80%"/>
   <br />
   <br /> 

 Enter the name of the domain "junicetechie.com"

  
35.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Thirty5.png?raw=true"  height="80%" width="80%"/>
   <br />
   <br />

 Provide login credentials of the domain controller for authentication and click "OK"


36.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Thirty6.png?raw=true"  height="80%" width="80%"/>
   <br />
   <br /> 

   Here click "Skip". We want the PC to authenticate credentials of the users from the domain.


37.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Thirty7.png?raw=true"  height="80%" width="80%"/>
   <br />
   <br />

  Restart now for the changes to take effect.

38.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Forty.png?raw=true"  height="80%" width="80%"/>
   <br />
   <br />

 The PC is now joined to the domain successfully. 

39.
   <p align="center">
   <img src="https://github.com/Eunice-Kamore/Creating-Windows-10-VM/blob/main/Images/Forty1.png?raw=true"  height="80%" width="80%"/>
   <br />
   <br /> 

Now in the next lab we will create new accounts in Active Directory and access the accounts from this Client PC. 
















