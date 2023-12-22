<h1>Azure Sentinel Lab</h1>


<h2>Description</h2>
In this lab I setup Azure Sentinel which is a SIEM and I connected it to a live virtual machine acting as a honey pot. I then observed how an invalid login attempt could be traced back to a certain location around the world. I used a pre-constrcuted PowerShell script to look up the geolocation information of the invalid login attempt and put it on the Azure sentinel map.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 

<h2>Environments Used </h2>

- <b>Azure Sentinel</b>  (SIEM)
- <b>Windows 10 Pro VM</b>  (Client)

<h2>Program walk-through:</h2>

<p align="center">
Properties of the honey pot (Windows VM) that I set up: <br/>
<img src="https://imgur.com/pHtAvVV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<p align="center">
The properties of the log analytics workspace setup I used to eventuallly create custome logs: <br/>
<img src="https://imgur.com/P2wd1IA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<p align="center">
A display of the security and servers I turned on: <br/>
<img src="https://imgur.com/xbvvZTY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<p align="center">
Selected for the Windows VM to ingest all events, not just certain types: <br/>
<img src="https://imgur.com/kYsRmzO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<p align="center">
An image of me accessing the Windows client: <br/>
<img src="https://imgur.com/o1l0AiL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<p align="center">
All three profiles of the Windows Defender Firewall have been turned off so the VM can be accessed from a remote device: <br/>
<img src="https://imgur.com/ixvgMAV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<p align="center">
A test to make sure the PowerShell script works and that the VM is accessible to remote devices: <br/>
<img src="https://imgur.com/huBK9YF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<p align="center">
The logs that were created from the PowerShell script as can be seen from the RawData: <br/>
<img src="https://imgur.com/4kG9MaF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<p align="center">
The custom log that was made after extracting the RawData: <br/>
<img src="https://imgur.com/gN03e04.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<p align="center">
The geolocation information depicted on a map of the user who failed to login to the Windows Client via RDP: <br/>
<img src="https://imgur.com/nBdF2QJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
