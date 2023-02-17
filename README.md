<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1: Create resources (Resource group, Windows VM & Ubuntu VM).
- Step 2: Connect to Windows VM and install Wireshark.
- Step 3: Initiate a non-stop ping from your Windows 10 VM to your Ubuntu VM.
- Step 4: Disable incoming ICMP traffic within Ubuntu VM Network Security Group.
- Step 5: Observe all changes to ICMP traffic in Windows 10 VM using Wireshark.
- Step 6: Enable all ICMP traffic again in Ubuntu VM and observe to ICMP traffic (should be resumed).
- Step 7: Observe SSH Traffic- filter SSH traffic in Wireshark, SSH into Ubuntu via private IP. 
          Once connected type different commands into SSH connection to observe SSH traffic spam.
- Step 8: Observe DHCP Traffic by filtering actiivty in Wireshark. Using command line (ipconfig /renew) in Windows 10 VM to
          attempt to issue new IP address for VM.Observe DHCP traffic in Wireshark.
- Step 9: In Wireshark filter out DNS traffic. Within command line use nslookup to look up IP addresses. For example, you could
          nslookup amazon.com or wikipedia.com. Oberve DNS traffic shown in Wireshark.
- Step 10: To observe RDP traffic filter out RDP activity in Wireshark. While in wireshark you should notice there's non-stop traffic spam.
           RDP traffic shows a continuous live stream of activity from one computer to another.
           
           



<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/Q1hS3DK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Screen capture shows example of ping from Windows VM to Ubuntu VM private IP.
</p>
<br />

<p>
<img src="https://i.imgur.com/Z8qmM1f.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 Disabling all inbound ICMP traffic on Ubuntu VM's Network Security Group.
</p>
<br />

<p>
<img src="https://i.imgur.com/ZdZf7Vq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 Using command line to nslookup Disney.com and Google.com IP addresses. This method is used to observe DNS filtered activity in Wireshark.
</p>
<br />
