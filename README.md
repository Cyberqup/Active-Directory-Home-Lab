<h1>Active Directory Home Lab</h1>

The purpose of this project is to set up a virtualised network environment for testing purposes. By creating a Domain Controller (DC) using Windows Server 2019 and a client machine using Windows 10 Pro within Oracle VirtualBox, you can simulate a typical IT infrastructure. This setup allows for hands-on experience with Active Directory (AD), network configuration, and user management. It provides a controlled environment to practice installing operating systems, configuring network settings, creating and managing user accounts, and understanding the interaction between a server and client in a domain.
<br />

<h2>Utilities Used</h2>
<table>
 <tr>
  <td>Window Server 2019</td>
  <td>Windows 10 Pro</td>
  <td>Active Directory Domain Services</td>
 </tr>
  <tr>
  <td>Domain Controller</td>
  <td>RAS / NAT</td>
  <td>Dynamic Host Configuration Protocol (DHCP)</td>
 </tr>
 <tr>
  <td>PowerShell ISE</td>
  <td>Oracle VirtualBox</td>
 </tr>
</table>
<br/>

<h2>Project Diagram</h2>
<p align="center">
<img src="https://i.imgur.com/3iB06uP.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />


 <h2>Prerequisites</h2>
<p align="center">
<h3>Oracle VirtualBox</h3>
• Download Oracle VirtualBox for Windows hosts from "https://www.virtualbox.org/wiki/Downloads"
 <br />
• Download the VirtualBox Extension Pack
 <br />
• Proceed through installation process to setup the application.
<br />
<br />
<h3>Windows 10</h3>
•  Download Windows 10 ISO image from "https://www.microsoft.com/en-us/software-download/windows10"
<br />
<br />
<h3>Windows Server 2019 </h3>
•  Download Windows Server 2019 ISO image from "https://www.microsoft.com/en-us/evalcenter/download-windows-server-2019"
<br />

 <h2>Approach</h2>
<h3>Create and Configure the First VM (Domain Controller):<br/></h3>
• Create a VM for the Domain Controller (DC) using the Server 2019 ISO.<br />
<h4> Assign two network adapters (NIC):<br /></h4>
• One for the Internet connectivity (external network).<br />
• One for the VirutalBox private network (internal network).<br />
• Install Server 2019 on the VM.<br />
<h4>Configure IP addressing:<br /></h4>
• Internal network: Assign static IPs.<br />
• External network: Obtain IP from the home router (DHCP).<br />
<br />
<br />

<h3>Setup the Domain Controller (DC):</h3>
• Name the server.<br />
• Install Active Directory (AD) and create the domain.<br />
• Configure Network Address Translation (NAT) and routing to allow clients on the private network to access the internet via the Domain Controller (DC).<br />
• Set up Dynamic Host Configuration Protocol (DHCP) on the Domain Controller (DC) for the internal network.<br />
<br />
<br />

<h3>Automate User Creation:</h3>
• Run a PowerShell script on the Domain Controller (DC) to create 1,000 user accounts in Active Directory (AD).<br />
<br />
<br />

<h3>Create and Configure the Client1 VM:</h3>
• Create a second VM (Client1) using the Windows 10 Pro ISO.<br />
• Connect Client1 to the private VirtualBox Network.<br />
• Log into Client1 using one of the domain accounts created by the PowerShell script.<br />
<br />
<br />
