# ticket-lifecycle
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Ticket Lifecycle: Intake Through Resolution</h1>
This tutorial outlines the lifecycle of a ticket from intake to resolution within the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to create, work, and resolves tickets within osTicket](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Ticket Lifecycle Stages</h2>

- Intake
- Assignment and Communication
- Working the Issue
- Resolution

<h2>Lifecycle Stages</h2>

<p>
https://1drv.ms/i/c/7ccef0ae451cd3d6/IQDMcz2_kIDdSbUBrfb8d__sAYc3pT7zETETLjUSu4Kpf8I?e=NRB2Pw
</p>
<p>
In this step, I started setting up my virtual machine in Microsoft Azure. I selected Windows 10 Pro version 22H2 (x64 Gen2) as the operating system and confirmed the x64 architecture since the selected image doesn’t support ARM64. For the VM size, I chose Standard D2s v3, which provides 2 virtual CPUs and 8 GB of memory. I picked this option because it offers a good balance between performance and cost for the task I’m working on. I also looked at additional options like the Azure Spot discount and hibernation, but hibernation isn’t supported with the VM size I selected. After that, I created the administrator account by setting a username and password, which will be used later to access the virtual machine once it’s deployed. With these settings configured, the setup is ready for the next steps, such as configuring disks and networking before reviewing and creating the VM.

</p>
<br />

<p>
https://1drv.ms/i/c/7ccef0ae451cd3d6/IQB0D8cYQVlgTKm4pfwU03qxAZ-cvIOcEt1XyvgywNLj1g4?e=83QFkM
</p>
<p>
In this step, I connected to the virtual machine I created in Azure using Remote Desktop. When attempting to connect, a certificate warning appeared saying that the certificate could not be verified because it was not from a trusted certifying authority. This is a common message when connecting to a newly created VM. Since I expected this and knew the VM I created was safe, I continued with the connection by accepting the warning. I then used the administrator credentials I set earlier to log in to the virtual machine. After confirming the connection, the remote session opened and allowed me to access and control the Windows environment running on the Azure VM
<br />

<p>
https://1drv.ms/i/c/7ccef0ae451cd3d6/IQCIia5bh53LQonBIhRxyBrWAdTuLzw640zJUbBxoftAp_A?e=1BmYtv
</p>
<p>
In this step, I extracted the compressed folder that contains the osTicket installation files. After downloading the zipped file, I used the built-in Windows extraction tool to unzip it to a folder on the desktop called osTicket-Installation-Files. I kept the default extraction location so it would be easy to find the files during the installation process. I also left the option checked to show the extracted files once the process finished. This step prepares the necessary installation files so they can be accessed and used in the following steps when setting up osTicket on the virtual machine.
</p>
<br />
https://1drv.ms/i/c/7ccef0ae451cd3d6/IQBC-nW7MUgLS62Lw8wV_U5vAdMLdGE8uRm2mqBM_P3E1vI?e=ebVMUe

In this step, I opened the Advanced Security Settings for the ost-config.php file located in the osTicket installation directory. This file is important for the setup process because it stores configuration settings for the application. To continue with the installation, I needed to review and modify the file’s permissions. Inside the security settings, I checked the current ownership and permission entries to make sure the correct users or groups would be able to access and modify the file if needed. Adjusting these permissions is an important step to ensure that the osTicket installer can properly write the required configuration settings during the installation process.

https://1drv.ms/i/c/7ccef0ae451cd3d6/IQAZHTKLkOOBQqQxQWeX6IplAbLXkjgieGhAWE2nId-RET0?e=dC16h4

In this scenario, I needed to update an agent’s password within the osTicket admin panel. While managing agent accounts, I selected the agent profile and opened the Set Agent Password option. Instead of manually setting a password, I chose to send the agent a password reset email so they could securely create their own password. This is a common practice in help desk environments because it helps maintain security and ensures that only the user knows their credentials. After selecting the option to send the reset email, the agent would receive instructions to set a new password and regain access to their account.











