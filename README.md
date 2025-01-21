<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Configuring Group Policy and Managing Accounts</h1>
This tutorial outlines Configuring Group Policy and Managing Accounts<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1 Dealing with Account Lockouts
- Step 2 Enabling and Disabling Accounts
- Step 3 Observing Logs
- Step 4

<h2>Dealing with Account Lockouts</h2>

![image](https://github.com/user-attachments/assets/2862de21-e154-4b52-8bd2-7d19fe5edecc)

<p>
Get logged into dc-1
</p>

![image](https://github.com/user-attachments/assets/b55206c6-d672-4d05-8daf-cd0675a55494)

<p>
Open Group Policy Management
</p>

![image](https://github.com/user-attachments/assets/12315ea0-e7c6-4525-be65-a0b6abcb800e)

<p>
Edit Default Domain Policy and link Group Policy to (mydomain.com)
</p>

![image](https://github.com/user-attachments/assets/976fe198-cbba-4dfa-91da-bdb2c7c1257f)

<p>
Select Account Lockout Policy
</p>

![image](https://github.com/user-attachments/assets/570a300a-6fcc-4e28-9a90-a506a2670353)

<p>
Configure Group Policy to Lockout the account after 5 attempts
</p>

![image](https://github.com/user-attachments/assets/7a8f20c5-10f2-43dd-8b2d-60b6541ebc92)

<p>
Log into Client1
</p>

![image](https://github.com/user-attachments/assets/140d33de-2e38-49d4-8fe7-adbb10225b4f)

<p>
Run Command Prompt as Administrator
</p>

![image](https://github.com/user-attachments/assets/0e2c103f-9519-4472-8269-b59051cf37f9)

<p>
Run (gpupdate /force) to update Group Policy and Verify the the Group Policy has been updated
</p>

![image](https://github.com/user-attachments/assets/acba1c5a-939a-48bd-897a-8b1c97726f6c)

<p>
Pick a random user account and attempt to log in with it 6 times with a bad password
</p>

![image](https://github.com/user-attachments/assets/fbc429ad-0b1e-41e9-81c5-d2c09bc78af6)

<p>
Go to the selected account user’s properties and unlock the account
</p>

![image](https://github.com/user-attachments/assets/2aefc995-c30e-40ab-b8ba-d43ed083b434)

<p>
You can also reset the User’s password by right-clicking the users name
</p>


<p>
Lorem ipsum dolor sit amet, 
</p>


<p>
Lorem ipsum dolor sit amet, 
</p>


<p>
Lorem ipsum dolor sit amet, 
</p>


<p>
Lorem ipsum dolor sit amet, 
</p>


<p>
Lorem ipsum dolor sit amet, 
</p>


<p>
Lorem ipsum dolor sit amet, 
</p>


<p>
Lorem ipsum dolor sit amet, 
</p>
