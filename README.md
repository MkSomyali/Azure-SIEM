<h1>Microsoft Azure SIEM: Failed RDP Logins Source IP to full GeoData Conversion from Windows Event Log</h1>


<h2>Description</h2>
A Powershell script parsing Windows Event Log information for failed RDP attacks on a Windows 10 pro virtual machine and a third party API is collecting geographic information about the attackers location. Microsoft Azure Sentinel displays the information on a world map.
<br />


<h2>Languages Used</h2>

- <b>PowerShell:</b> Extracting RDP failed logon logs from Windows Event Viewer

<h2>Environments Used </h2>

- <b>Microsoft Azure:</b> Virtual Machine, Log Analytics Workspace, Mircorsoft Sentinel

- <b>Windows 10 pro:</b> (21H2)

<h2>Utilities Used</h2>

- <b>ipgeolocation.io:</b> IP Address to Geolocation API

<h2>Lab walk-through:</h2>

<p align="center">
Create Virtual Machine: Open Firewall to public internep traffic <br/>
<img src="https://imgur.com/DkaG4pN.png" width="80%" alt="Attack monitoring Steps"/>
<br />
<br />
Create Log Analytics Workspace: Connect Log Analytics to VM  <br/>
<img src="https://imgur.com/KWZN4Xd.png" height="80%" width="80%" alt="Attack monitoring Steps"/>
<br />
<br />
Set up Microsoft Azure Sentinel: Log into VM remotely <br/>
<img src="https://imgur.com/2IDgZxq.png" height="80%" width="80%" alt="Attack monitoring Steps"/>
<br />
<br />
Observe Event Viewer Logs in VM: Turn off Windows Firewall on VM  <br/>
<img src="https://imgur.com/6HA10WR.png" height="80%" width="80%" alt="Attack monitoring Steps"/>
<br />
<br />
Get Geolocation.io API Key: Run Powershell script to get Geo Data from attackers  <br/>
<img src="https://imgur.com/nFNNGVH.png" height="80%" width="80%" alt="Attack monitoring Steps"/>
<br />
<br />
Create custom log in LAW: Extract filds from raw custom log data  <br/>
<img src="https://imgur.com/3nu9aY8.png" height="80%" width="80%" alt="Attack monitoring Steps"/>
<br />
<br />
Setup map in Sentinel by Country: Observe attackers on world map <br/>
<img src="https://imgur.com/9i067XT.png" height="80%" width="80%" alt="Attack monitoring Steps"/>
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
