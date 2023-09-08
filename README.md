<h1>Active Directory Home Lab</h1>


<h2>Description</h2>
In this lab, I created an Active Directory home lab Environment using Oracle Virtual Box.  This developed my understanding of how home directory and Windows networking work. I simulated an Enterprise Network Deployment in HomeLab: Setup a Domain Controller, Active Directory, and 1000+ Users using PowerShell Script. This concept was to allow all clients/ computers added to the domain to communicate with the Domain controller through the internal NIC and the DC to internet NIC for the clients to get internet access.
This entails the following:

- <b>Active Directory Domain Services/ Domain: This allows admins to manage and store information about resources from the network.</b> 
- <b>RAS/NAT: This allows the client to access internet resources.</b>
- <b> Dynamic Host Configuration Protocol: This automatically provides and assigns IP addresses to the client device.</b> 
- <b>Powershell Script: This was used to create users on the active directory.</b>
- <b> Windows 10 Client: This was connected to the network to test the domain controller.</b>
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Oracle Virtual Box</b>

<h2>Environments Used </h2>

- <b>Windows 10</b>
- <b>Windows Server 2019</b>
<h2>Program walk-through:</h2>

<p align="center">
The different network interfaces cards used: <br/>
<img src="https://imgur.com/nrxZXHg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Server Manager Dashboard:  <br/>
<img src="https://imgur.com/uW1DPYr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Login into created Admin Account:  <br/>
<img src="https://imgur.com/ZOGOm7Y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Names to be added to Active Directory: <br/>
<img src="https://imgur.com/pFpKXFB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Use of Powershell script to create users:  <br/>
<img src="https://i.imgur.com/.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
One of the created users:  <br/>
<img src="https://imgur.com/DSlA165.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Already added Windows 10 client to the domain:  <br/>
<img src="https://imgur.com/1PrdbZW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Testing connectivity to the domain and internet:  <br/>
<img src="https://imgur.com/U74Is1x.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h2>Step-by-Step guide on the Setup</h2>

<b>Virtualization Installation</b>

  - Install Virtual Box
  - Install Virtual Machines (Windows Server 2019 and Windows 10)

<b>On the Windows Server</b>
  - Identify which of the network interface cards will be the internal NIC and Internet NIC.
  - Manually assign the IP address to the internal NIC and leave the Internet NIC for DHCP to automatically assign the IP address.
  - Rename Windows Server.

<b>Setup Active Directory Domain Services</b>

  - Install Active Directory Domain Services.
  - Add roles and features.
  - Promote the DC.
  - Create a dedicated admin account.
  - Make the created account the domain admin.

<b>Install NAT/RAS (This allows the Windows client to connect to the internet)</b>
  - Add roles and feature → + Remote access → + routing.
  - Configure and enable routing from routing and remote management tools  → + Install NAT.

<b>Install DHCP (This will automatically assign IP address to the Windows client)</b>

  - Add roles and feature.
  - Authorize and refresh Domain DHCP.
  - Create the scope of IP addresses to be assigned to clients(This is to give a range of IP addresses that can be assigned to computers on the domain) optionally, you can restrict IP addresses to be issued to clients by the DHCP and also assign the time IP addresses could be on lease for.

<b>Add Users to the Domain</b>
  - PowerShell script can be used to automatically add/ create users on the domain.
  - Admin User and Features application → + New “Organizational Unit” → + New “User” to manually create users.

<b>Boot the Windows 10 client</b>

  - Configure the client to be a member of the domain.
  - Login as one of the created users.

<b>Check Active Directory for address leases and computers connected to the Domain</b>

  - On the DC, Active Directory Users and Computers → domain → computers (To check connected computers on the domain).
  - DHCP → Domain → ipv4 → Scope → Address leases (To check the address given to clients on the  domain).
    
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
