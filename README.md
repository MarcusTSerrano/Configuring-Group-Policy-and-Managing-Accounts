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

- Step 1 Configuring Group Policy and dealing with Account Lockouts
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

![image](https://github.com/user-attachments/assets/d3883523-264b-471c-8cdc-878440112ff1)

<p>
You can also reset the User’s password by right-clicking the users name
</p>

![image](https://github.com/user-attachments/assets/63980287-2bf1-4dda-bd68-c248dfe11dbe)

![image](https://github.com/user-attachments/assets/385fdbfe-41ef-4f27-aec9-057617b193c5)



<p>
Attempt to login with the User Account
</p>


<h2>Enabling and Disabling Accounts</h2>

![image](https://github.com/user-attachments/assets/c8eb855a-5e88-4550-b02a-f903021d63a5)


<p>
Disable the same account in Active Directory
</p>

![image](https://github.com/user-attachments/assets/060ed14e-311e-4b3a-b673-2911f1335c52)

![image](https://github.com/user-attachments/assets/08413cbd-5542-4b52-8dfe-b3bb8917cfe9)

<p>
Attempt to login with it, observe the error message
</p>

![image](https://github.com/user-attachments/assets/9a83a615-1c49-4550-a94f-89de5bb93fc2)

![image](https://github.com/user-attachments/assets/03db616f-84ae-43d6-b282-379766eafcc6)

<p>
Re-enable the account and attempt to login with it.
</p>


<h2>Observing Logs</h2>


![image](https://github.com/user-attachments/assets/f83d8223-9369-4a16-bf62-992ba744195e)

<p>
In the Domain Controller open Event Viewer by searching (eventvwr.msc)
</p>

![image](https://github.com/user-attachments/assets/a261ae8d-e7c3-4a51-8a6d-c39f6cf75976)

![image](https://github.com/user-attachments/assets/53582768-2718-45d0-a6b0-098564bae4b3)

<p>
Windows Logs > Security to observe the logs (you can filter by using the User’s name)
</p>
