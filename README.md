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

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
