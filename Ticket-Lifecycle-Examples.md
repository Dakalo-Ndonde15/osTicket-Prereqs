<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Ticket Lifecycle: Intake Through Resolution</h1>

- This tutorial outlines the lifecycle of a ticket from intake to resolution within the open-source help desk ticketing system osTicket. 
- In this lab, we will be creating tickets as end users Observing all the ticket properties and responding to them as help desk professionals
<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to create, work, and resolves tickets within osTicket]()

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Ticket Lifecycle Stages</h2>

- Intake
- Assignment and Communication
- Working the Issue
- Resolution

<h2>Project Walk-through:</h2>

<h4>Change the SysAdmins Department to a Top Level Department.</h4>

<p>
  <img src="https://i.imgur.com/uQ5LZzm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/MbOHcjS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4> DELETE the Maintenance Department (not archive)</h4>

<p>
  <img src="https://i.imgur.com/Zbu5JBu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<h4>As an end-user, create the following ticket</h4>
entire mobile/online banking system is down
<p>
  <img src="https://i.imgur.com/Uk8R1B2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<h4>Configure Roles (for grouping permissions)</h4>

- Admin Panel -> Agents -> Roles
    - Supreme Admin

<p>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Configure Departments (Ticket Visibility, Help Desk vs SysAdmins, vs Networking)</h4>

- Admin Panel -> Agents -> Departments
    - SysAdmins

<p>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Configure Teams</h4>

- Admin Panel -> Agents -> Teams (Pull Agents from different Departments)
    - Online Banking

<p>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Allow anyone to create tickets</h4>

- Admin Panel -> Settings -> User Settings (UNCHECK: unregistered users can create tickets)
    - Registration Required: Require registration and login to create tickets

<p>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Configure Agents (workers)</h4>

- Admin Panel -> Agents -> Add New
    - Jane (Dept: SysAdmins)
    - John (Dept: Support)

<p>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Configure Users (customers)</h4>

- Agent Panel -> Users -> Add New
    - Karen
    - Ken

<p>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Configure SLA</h4>

- Admin Panel -> Manage -> SLA
    - Sev-A (Grace Period: 1 hour, Schedule: 24/7)
    - Sev-B (Grace Period: 4 hours, Schedule: 24/7)
    - Sev-C (Grace Period: 8 hours, Business Hours)

<p>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />

<h4>Configure Help Topics (For when users create a ticket)</h4>
- Admin Panel -> Manage -> Help Topics
    - Business Critical Outage
    - Personal Computer Issues
    - Equipment Request
    - Password Reset
    - Other

<p>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />
  
[<h4>Finally done!</h4>
