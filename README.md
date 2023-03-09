<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This repository outlines my knowledge on the post-install configuration of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles
- Configure Departments
- Configure Teams
- Allow anyone to create tickets
- Configure Agents (workers)
- Configure Users (customers)
- Configure SLA
- Configure Help Topics

<h2>Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/gm0yDpY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the virtual machine, browse to the log in page of osTicket with the URL: http://localhost/osTicket/scp/login.php
  
Log in with the admin credentials that were created.
<br />

<p>
<img src="https://i.imgur.com/9TSOUr3.png" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Right when you log in, you will be in the agent panel of osTicket. You can tell whether you are in the "Agent" or "Admin" panel by what you see in the uper right corner of the screen. When you are in the Agent panel, the tab on the upper right will have the option to switch to the Admin panel (and vice versa). You can see this demonstrated by what is highlighted in red in the screenshot above.
</p>
<br />

<p>
<img src="https://i.imgur.com/fZzZ2Uz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Configuring Roles:
  
Navigate to the Admin panel (you can tell you are in the Admin panel because you have the option to witch to the Agent panel)
  
From there, click the tab labeled: Agents > Roles > Add New Role
</p>
<br />

<p>
<img src="https://i.imgur.com/V9Nmcgf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Name the new role "Supreme Admin" > Click on the "Permissions" tab.
</p>
<br />

<p>
<img src="https://i.imgur.com/73RFZAO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Check all of the permissions under the "Tickets", "Tasks" and "Knowledgebase" tabs > click "Add Role".
</p>
<br />

<p>
<img src="https://i.imgur.com/Ewa30kI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Configuring Departments:
  
Admin Panel > Agents > Departments > Add New Department
</p>
<br />

<p>
<img src="https://i.imgur.com/a8Xkawr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Name the department: "System Administrators" > Create Dept
  
</p>
<br />

<p>
<img src="https://i.imgur.com/Pz2ZiUG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Configuring teams:
  
Admin Panel > Agents > Teams > Add New Team
</p>
<br />

<p>
<img src="https://i.imgur.com/H7vsxVv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Name the team: "Level II Support" > Members > Add yourself as a team member with the drop-down menu > Create Team
</p>
<br />

<p>
<img src="https://i.imgur.com/77hbaJy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Allow anyone to create tickets: 
  
Admin Panel > Settings > Users > Authentication Settings
  
Make sure the "Registration Required" box is UN-checked
</p>
<br />

<p>
<img src="https://i.imgur.com/RY8Lp6W.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Configuring Agents (workers):
  
Admin Panel > Agents > Add New Agent
</p>
<br />

<p>
<img src="https://i.imgur.com/Hf7dUlr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create an agent by the name of Jane Doe with the credentials in the screenshot above and then create a password that does not have to be reset. Click on the "Access" tab and under "Primary Department" choose the System Administrators department. Select the Supreme admin role. Click on the "Teams" tab and select the "Level II Support" team. Click "Create".
  
Go back to Agents > Add New Agent
  
Create another agent by the name of John Doe with the same steps for the credentials. Click on the "Access" tab and under "Primary Department" choose the "Support" department. Select the "View only" role. Under the "Extended Access" drop-down menu choose "Support". Click "Create".
</p>
<br />

<p>
<img src="https://i.imgur.com/MaJXXgu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Configuring Users (customers):
  
Agent Panel > Users > Add User
  
Create a user by the name of Karen with the credentials above > Add User
  
Create another user by the name of Ken with the same credentials replaced with "Ken" > Add User
</p>
<br />

<p>
<img src="https://i.imgur.com/rKfdNif.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Configuring SLA:
  
Admin Panel > Manage > SLA > Add New SLA Plan
</p>
<br />

<p>
<img src="https://i.imgur.com/EPbbzMX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create three SLA Plans:
  
Sev-A (1 hour, 24/7)
  
Sev-B (4 hours, 24/7)
  
Sev-C (8 hours, business hours)

</p>
<br />

<p>
<img src="https://i.imgur.com/qdqQFdV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Configuring Help Topics:
  
Admin Panel > Manage > Help Topics > Add New Help Topic
</p>
<br />

<p>
<img src="https://i.imgur.com/2ZVDl6K.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create four Help Topics:
  
Business Critical Outage (Top Level Topic)
  
Personal Computer Issues (Top Level Topic)
  
Equipment Request (Top Level Topic)
  
Password Reset (Top Level Topic)
  
That concludes the configuaration aspect of the osTicket system! In the next repository I will be going over Tickets and Ticket Lifecycle.
</p>
<br />
