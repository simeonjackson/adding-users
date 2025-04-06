<h1>Adding Users to Active Directory with PowerShell</h1>
I created a script in PowerShell to take usernames from a CSV file to add users to my Active Directory setup. While not proficient in PoSH yet, I was able to create this script with a bit of technical oversight from ChatGPT. <br />


<h2>Environments and Technologies Used</h2>

- PowerShell
- ChatGPT
- Active Directory Users and Computers

<h2>Operating Systems Used </h2>

- Windows Server 2022

<h2>Deployment and Configuration Steps</h2>

<p>
To accompany my Active Directory lab, I made a script in PowerShell to create users for my domain. I did this by using a CSV file and a PowerShell script that will create users in my "Employees" organizational unit (OU).
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
I used ChatGPT to create a basic CSV file with my names and usernames for my employees and I saved this to my C: drive.
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
Using the following script I can take the data in the file and create users in my lab environment.
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
The first lines tell the script where to find the "users" CSV file and the second line reads this file and stores it.
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
I created a generic password for each user. Obviously this would not be used in a real environment where we would want to use strong, unique passwords for each individual account.
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
This line specifies the location within Active Directory where the new users will be placed. Which is in the OU "employees" on the "mydomain" domain.
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<p>
The next set of code creates individual user accounts for each row in the CSV. Specifying the user's full name, account name, password we set, and the organizational unit where the user account will be created. The "Enabled" line ensures that the account is enabled by default.
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
Here is the result of running this script:
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
This script automates the process of creating multiple user accounts, saving time and reducing errors compared to manual creation.
</p>
