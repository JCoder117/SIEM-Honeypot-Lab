<h1>SIEM Honeypot Lab</h1>

<h2>Description</h2>

A SIEM honeypot utilizing Azure Sentinel as a SIEM and connecting it to a live virtual machine acting as a honeypot. This honeypot allowed for the observation of live attacks by brute force from attackers around the world. In addition a custom powershell script to analyze the attackers geolocation which was then plotted in Azure Sentinal Map.

<br />


<h2>Enviornments, Languages and Utilities Used</h2>

- <b>Azure</b> 
- <b>Sentinel</b>
- <b>Powershell</b>
- <b>Virtual Box</b>
- <b>Windows 10</b>

<h2>Program walk-through:</h2>

<p align="center">
Creating Honeypot: <br/>
<img src="1. Creating Honeypot.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Password Creation:  <br/>
<img src="2. Creating Password HyperLethal101!.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Virtual Machine Firewall: <br/>
<img src="3. NIC is the firewall.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Removing Firewall:  <br/>
<img src="4. Removing the firewall to open the VM to the open internet.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Allowing for traffic to discover vm:  <br/>
<img src="5. Opening up the VM to be discovered by all traffic.png
" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Allowing for traffic to discover vm pt.2:  <br/>
<img src="6. Opening up the VM to be discovered by all traffic 2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Log ingestion from vm to workspace for geolocation:  <br/>
<img src="7. Log Analytics purpose to ingest logs from the virtual machine the traffic will contain geographic location they will be stored in the log analytics workspace.png"/>
<br />
<br />
Data and Log collection:  <br/>
<img src="9. Collecting all data and logs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Connecting workspace to vm(honeypot):  <br/>
<img src="10. Connecting the Log Analytics workspace to my vm that is my honeypot.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sentinel as SIEM for visualization:  <br/>
<img src="11. Utilizing microsoft sentinel as my siem (Security Information and Event Managment) to visualize the attack data.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Connecting to VM from remote desktop:  <br/>
<img src="12. Logging into Virtual Machine from remote desktop connection.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Event viewer for geomapping:  <br/>
<img src="13. Utilizing event viewer in the vm to use for the geo map.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Attempting login to prove failure:  <br/>
<img src="14. Attempted login test for logging into vm (failure).png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Attempted failure display alert:  <br/>
<img src="15. Failure attempt display on RDC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Login Failure:  <br/>
<img src="16. Logon fail.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Failure displayed in Remote Connection:  <br/>
<img src="17. Displaying the failed login attempt done from RDC to get into VM TheEmile.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
IP address collection:  <br/>
<img src="18. IP addresses will be collected and placed into ipgeolocation.io to identify where they are coming from.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Firewall ping test (on):  <br/>
<img src="19. Pinging my VM with the firewall turned on.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Firewall turned off for traffic:  <br/>
<img src="20. Turning off firewall on VM to enable traffic turned off in the domain, private, and public.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Firewall ping test (off):  <br/>
<img src="21. Turning off firewall within VM allowed me to ping the vm from my personal desktop enabling the vm to be vulnerable to login attempts and traffic.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Powershell script for capture:  <br/>
<img src="22. Using Powershell script to capture failed login attempts and collecting their information using ipgeolocation.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Failed attempted being captured:  <br/>
<img src="23. Data of the failed login attempts in Event Viewer being collected from the powershell script.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Custom log from gathered log file from VM training log analytics:  <br/>
<img src="24. Creating a custom log from the log file from the virtual machine from powershell to train log analytics on what to look for.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observing collected data from event manager/data:  <br/>
<img src="25. Viewing the securityevent manager and data collected from azure in reference to the vm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Display of failed login attempts equal to 4625:  <br/>
<img src="26. Displaying the failed login attempts which is equal to EventID == 4625.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Failed remote desktop protocl logins:  <br/>
<img src="27. Running the Failed_RDP_with_geo custom log this displays all of the attempted logins being done on the VM based on the training given to it from the training information from the failed_rdp.log.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
KQL query for categorization:  <br/>
<img src="28. Utilized KQL query to categories information coming from the powershell script from the Security Event this query then outlined where the attacks were coming from on the map.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Mapping of attacks:  <br/>
<img src="29. Map displaying where the attacks came from.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Real-time attempts of logins from vm:  <br/>
<img src="30. Real-time login events from vm powershell ISE based upon SecurityEvent windows log.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Updated world map after 10 minutes:  <br/>
<img src="31. Update world map after being live for 10 minutes.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
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
