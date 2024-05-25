<h1>Failed RDP Azure Honeypot With Geo Mapping</h1>

<h2>Description</h2>
This project consists of setting up a live honeypot in Azure, consisting of the following components, a VM with firewall removed which is then connect to the Log Analytics Workspace in Azure. We then use the logs obtained in the Sentinel (SIEM) to plot our attackers approximated geolocations based on their IP's longitude and lattitude.  
<br></br>
<p>
Setup:<br/>  
</p>

![image](https://github.com/ioritzeguileor/FailedRDP_Honeypot/assets/66511137/320a26c9-c5dd-4802-9e04-93175cbfc219)


The Powershell script found in the repository is responsible for extracting the data from the security events and then using the IP's obtained from the log to put it though an external API which can help us grab the attackers lattitude and longitude, we can then store those and use them in our SIEM to plot their geolocation.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell : Use script to extract logs and grab latitude and longitude from IP using [IP Geolocation](ipgeolocation.io) API Key</b> 
- <b>KQL : Query extracted logs in order to display latitude and longitude correctly on Map</b>
<p align="center">
<img src="https://i.imgur.com/szKaePC.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)


<h2>Attacks from Brazil coming in; Custom logs being output with geodata</h2>

<p align="center">
<img src="https://i.imgur.com/uElyDW2.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<h2>World Map 24 Hours After Upload</h2>

<p align="center">
<img src="https://i.imgur.com/krRFrK5.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
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
