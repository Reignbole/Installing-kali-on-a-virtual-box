# Installing-kali-on-a-virtual-box
A step-by-step guide to installing and setting up Kali Linux on VirtualBox. Includes pre-configured settings, troubleshooting tips, and optimization tweaks for better performance.
# Setting_up_Kali_linux_virtual_machine
<strong>Installing Kali Linux on Windows Using VirtualBox</strong>
<p>This guide provides a detailed step-by-step process for absolute beginners to install Kali Linux on a Windows machine using VirtualBox. Follow the steps carefully and refer to the screenshots provided in the GitHub repository for clarity.</p>

<strong>Prerequisites</strong>
1.	Windows Machine: Ensure your computer runs a 64-bit version of Windows.
2.	Virtualization: Enable virtualization in your BIOS/UEFI settings.
3.	Software Requirements:
o	VirtualBox (latest version)
o	Kali Linux ISO (Installer image)
<img src="Folder/Download Kali.png">
_________________________________________________________________________________________________________________
Steps to Install Kali Linux

<strong>Step 1: Enable Virtualization on Windows</strong>
1.	Restart your computer.
2.	Enter the BIOS (BAsci input and Output system) /UEFI (Unified Extensible Firmware Interface) settings (commonly accessed by pressing DEL, F2, or F12 during boot).
3.	Locate Virtualization Technology or Intel VT-x/AMD-V.
4.	Enable it and save the changes.
5.	Reboot your computer.

<strong>Step 2: Install VirtualBox</strong>
1.	Download the VirtualBox installer from the official website.
2.	Run the installer.
3.	Follow the installation wizard:
<ul>
  <li>Click Next for default settings.</li>
  <li>Accept any prompts to install necessary drivers.</li>
</ul>

4.	Launch VirtualBox after installation.

<strong>Step 3: Download Kali Linux ISO</strong>
1.	Visit the Kali Linux download page.
2.	Download the Installer Image (choose 64-bit).
3.	Extract file from downloads

<img src="Folder/Extract file.jpg">	

<strong>Step 4: Create a New Virtual Machine in VirtualBox</strong>
1.	Open VirtualBox and click New.
	
<img src="Folder/New.jpg">	
	
2.	Fill out the fields:
  o	Name: Kali Linux
  o	Type: Linux
  o	Version: Debian (64-bit)
3.	Click Next.
<img src="Folder/Name your OS.png">
		
4.	Assign memory (RAM): Select at least 2048 MB (2 GB) or more, depending on your system's capacity.
5.	Select Create a Virtual Hard Disk Now, then click Create.	
6.	Choose VDI (VirtualBox Disk Image) and click Next.
7.	Choose Dynamically Allocated and click Next.
8.	Specify the disk size (minimum 20 GB) and click Create.

<img src="Folder/Create HDD.png">	

<strong>Step 5: Configure the Virtual Machine</strong>
1.	Select the newly created virtual machine and click Settings.
2.	Go to System > Processor:
  o	Assign at least 2 CPUs.
3.	Go to Display:
  o	Set Video Memory to the maximum.
4.	Go to Storage:
  o	Ensure the virtual disk image is correctly attached.
5.	Click OK to save settings.

<img src="Folder/kal 5.png">	
6. configure Linux Network settings to Bridge Adapter

<img src="Folder/Linux Network.png">

<strong>Step 6: Start the Virtual Machine</strong>
1.	Select the Kali Linux VM and click Start.

<img src="Folder/Click on start.png">
 
2.	Kali Linux will boot up directly without the need of installation, as this is a pre-configured image.
3.	Log in with the default credentials:
  <strong>o	Username: kali</strong>
  <strong>o	Password: kali</strong>
4.	Change the default password for security:
    
<img src="Folder/Start your Linux VM.png">

<strong>Step 7: Install VirtualBox Guest Additions (Optional)</strong>
1.	go to Devices > Insert Guest Additions CD Image in VirtualBox once Kali Linux is running.
2.	Open the terminal in Kali Linux and run:
3.	sudo apt update

<img src="Folder/kal 11.png">
 
4.     sudo apt install -y virtualbox-guest-dkms virtualbox-guest-utils virtualbox-guest-x11

<img src="Folder/sudo apt upgrade -y.png">

5.	Restart the virtual machine.
________________________________________
Common Issues and Troubleshooting
•	Virtualization Disabled: Ensure it is enabled in the BIOS.
•	Error During Boot: Verify the integrity of the Kali Linux image.
•	Low Performance: Allocate more RAM and CPU cores to the VM.
