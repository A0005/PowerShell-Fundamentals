<h1>Windows PowerShell [01] Introduction</h1>

[YouTube Demonstration](https://www.youtube.com/watch?v=TUNNmVeyjW0&list=PL1H1sBF1VAKXqO_N3ZNP0aL15miJcUhw7)

<h2>Description</h2>
This project is about installing Windows Server 2022 on a Virtual Box and adding basic configurations like updating the Server Name, installing a Web Browser, installing Active Directory, IP configuration, and installing Exchange Server 2019.
<br />


<h2>Languages</h2>

- <b>PowerShell</b> 

<h2>Environments Used </h2>

- <b>Virtual Box</b>
- <b>Windows Server 2022</b>
- <b>Exchange Server 2019</b>

<h2>Program walk-through:</h2>

<!-- <p align="center"> --!>
1 - Download and Install Virtual Box <br/>
2 - Download and Install Windows 2022 Standard Edition with Desktop Experience on Virtual Box <br/>
3	- Rename the Server to a suitable name <br/>
4	- Download and Install Chrome or Brave browser or you can stick with Microsoft Edge <br/>
5	- Download and Install Unified Communications Managed Api 4.0 Runtime <br/>
6	- Download and Install Microsoft Visual C++ 2013 Redistributable (x64) <br/>
<img width="700" alt="Windows Server 2022 Installation" src="https://user-images.githubusercontent.com/103763124/185809379-a26cfde3-0f2a-4b1e-80a4-356b90f220b2.png"/>
<br />
<br />
7	- Install Active Directory Domain Services and Promote the Server to become a Domain Controller <br/>
8	- Change Ethernet Settings for IPV4 and IPV6 to obtain DNS Automatically <br/>
<img width="700" alt="Installation of AD DS" src="https://user-images.githubusercontent.com/103763124/185810048-0e9b6ad9-1821-4710-83f3-09119eee6205.png"/>
<br />
<br />
9	- Download Exchange 2019 and upload it using Virtual Box <br/>
10	- Installation Commands for Exchange Server 2019 <br/>

   • Open PowerShell and run as Administrator <br/>
   
   • Change into the directory that Exchange Server was uploaded to for example type d: <br/>
   
   • Type Install-WindowsFeature RSAT-ADDS <br/>
   
   • Install Required Roles Type Install-WindowsFeature NET-Framework-45-Features, RPC-over-HTTP-proxy, RSAT-Clustering, RSAT-Clustering-CmdInterface, RSAT-Clustering-Mgmt, RSAT-Clustering-PowerShell, Web-Mgmt-Console, WAS-Process-Model, Web-Asp-Net45, Web-Basic-Auth, Web-Client-Auth, Web-Digest-Auth, Web-Dir-Browsing, Web-Dyn-Compression, Web-Http-Errors, Web-Http-Logging, Web-Http-Redirect, Web-Http-Tracing, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Lgcy-Mgmt-Console, Web-Metabase, Web-Mgmt-Console, Web-Mgmt-Service, Web-Net-Ext45, Web-Request-Monitor, Web-Server, Web-Stat-Compression, Web-Static-Content, Web-Windows-Auth, Web-WMI, Windows-Identity-Foundation, RSAT-ADDS <br/>

   
   • Preparing Schema Type .\setup /PrepareSchema /IAcceptExchangeServerLicenseTerms <br/>
   
   • Preparing Active Directory Type .\setup /Preparead /IAcceptExchangeServerLicenseTerms /OrganizationName:"COMPANY" <br/>
   
   • Preparing Domain Type .\setup /Preparedomain /IAcceptExchangeServerLicenseTerms <br/>
<img width="700" alt="Installation of Exchange Server 2019" src="https://user-images.githubusercontent.com/103763124/185810069-5fd42893-4ca1-4b46-9b36-5c1b81698ef2.png"/>
<br />
<br />
11	- Open File Explorer and Right Click on the Exchange drive and click Install or Run Program from media <br/>
12	- Click on the start menu and expand the Exchange Folder Sever 2019 and select Exchange Administrative Center and login <br/>
<img width="700" alt="Exchange Server 2019" src="https://user-images.githubusercontent.com/103763124/185810089-b751148d-c4bc-4704-a578-376c030486dc.png"/>
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
