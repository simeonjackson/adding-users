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

![Screenshot 2025-02-27 223643](https://github.com/user-attachments/assets/5b433e59-297c-45a5-a6f5-3bd6c1298b85)


<p>
I used ChatGPT to create a basic CSV file with my names and usernames for my employees and I saved this to my C: drive.
</p>

![Screenshot 2025-02-27 125234](https://github.com/user-attachments/assets/e895bffe-494f-414d-8442-b95eb8f8f776)


<p>
Using the following script I can take the data in the file and create users in my lab environment.
</p>

![Screenshot 2025-02-27 165940](https://github.com/user-attachments/assets/dd6adb15-7fac-4228-b2e7-1b05201c8423)


<p>
The first lines tell the script where to find the "users" CSV file and the second line reads this file and stores it.
</p>

![Screenshot 2025-02-27 170018](https://github.com/user-attachments/assets/c73f60aa-5777-4935-9bdf-d915b875493d)


<p>
I created a generic password for each user. Obviously this would not be used in a real environment where we would want to use strong, unique passwords for each individual account.
</p>

![Screenshot 2025-02-27 170036](https://github.com/user-attachments/assets/5995f20e-670c-4b2c-b4f6-19c216fe6178)


<p>
This line specifies the location within Active Directory where the new users will be placed. Which is in the OU "employees" on the "mydomain" domain.
</p>

![Screenshot 2025-02-27 223421](https://github.com/user-attachments/assets/6987581b-9963-4fce-a910-d55d4908c77c)



<p>
The next set of code creates individual user accounts for each row in the CSV. Specifying the user's full name, account name, password we set, and the organizational unit where the user account will be created. The "Enabled" line ensures that the account is enabled by default.
</p>

![Screenshot 2025-02-27 170118](https://github.com/user-attachments/assets/5b7d38e3-b37a-4d9e-812c-cf1be991e0f8)


<p>
Here is the result of running this script:
</p>

![Screenshot 2025-02-27 223932](https://github.com/user-attachments/assets/4a6c9b38-3c76-4071-8e91-41c8df0b6eef)


<p>
This script automates the process of creating multiple user accounts, saving time and reducing errors compared to manual creation.
</p>
