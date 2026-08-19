# Zero-Trust-IAM-Implementation-Lab

<h2>Description</h2>
Scenario (MRG the fictional company used throughout this portfolio)

Meridian Retail Group recently underwent an internal security audit that flagged serious identity and access weaknesses.
1. Shared login credentials
2. No enforced MFA
3. Standing (always On ) admin privileges.
4. No conditional access policies.

<h2>Solution</h2>
I'll redesign meridian's access model around zero trust Framework "Never Trust, Always Verify" Using Microsoft Entra ID - leveraging their existing M365 E5 license.

<h2>Program walk-through:</h2>

<p align="center">
  Creating MRG users on Microsoft entra admin center <br/>
<img src="https://imgur.com/GsKq65b.png" height="65%" width="65%" alt="creating users"/>

<p align="center">
  <img src="https://imgur.com/Nr5Sbhz.png" width="65%" alt="Creating users">
  <img src="https://imgur.com/qn771fJ.png" width="65%" alt="Creating users">
</p>

<p align="center">
Created the Meridian security groups for all department <br/>
  <img src="https://imgur.com/yt5md4X.png" height="75%" width="75%" alt="Security Groups">
  

<p align="center">
  <br>Created a break-glass emergency access account to provide a secure recovery path into the environment in the event that a Conditional Access policy inadvertently locks out administrators or users.<br/> 
 <img src="https://imgur.com/kAPsZLB.png" height="75%" width="75%" alt="Break-glass"/>



  <div align="center">

> ## 🔴 Break-Glass Account
>
> **☁️ Cloud-Only** — Not synchronized from on-premises Active Directory.  
>
> **🔑 Non-Expiring Password** — Password does not expire and MFA is not enrolled.  
>
> **👑 Global Administrator** — Role assigned directly, not through PIM.  
>
> **🚫 CA Exclusion** — Excluded from all Conditional Access policies.

</div>
 

<br><br> 
<p align="center">
 Implementing Conditional Access Policy<br/>

<div align="center">

<table>
<tr>
<td align="center" width="33%">

### 🔐 CA001
**Require MFA for All Users**

</td>
<td align="center" width="33%">

### 🛡️ CA002
**Block Legacy Authentication**

</td>
<td align="center" width="33%">

### 💻 CA003
**Require Compliant Device**

</td>
</tr>
</table>

</div>
