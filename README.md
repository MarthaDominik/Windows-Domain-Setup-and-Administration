# Windows Domain Setup and Administration

In this project, I demonstrated the process of setting up and administering a **Windows Domain** environment, showcasing key network administration and security management skills. The project covered important aspects such as user account creation, device management, security policy implementation, and central control using **Active Directory** and **Group Policy Objects (GPOs)**.

**Key Areas Covered:**

• **Windows Domain Setup and Configuration:** Establishing a centralized network environment using **Active Directory** to manage resources, users, and devices efficiently.

• **User Account and Device Management:** Creating, managing, and organizing users and computers in **Organizational Units (OUs)** within Active Directory for better control and management.

• **Security and Permissions:** Implementing security policies, such as password policies and user access controls, to maintain a secure environment. This included enforcing password complexity requirements and restricting user access to sensitive system settings like the **Control Panel**.

• **Scalability and Efficiency:** Demonstrating how centralized management simplifies network operations for hundreds of users and devices across multiple locations, reducing manual configurations and enhancing administrative efficiency.

## Launching Active Directory Users and Computers (ADUC)

In this step, I opened the **Active Directory Users and Computers (ADUC)** tool from the Windows Start menu. This tool is used for managing users, groups, and computers in a Windows Domain.

ADUC is the central interface for managing the directory services provided by **Active Directory**. It allows administrators to create, modify, and manage users, computers, and other objects within a domain. This is the starting point for managing the Active Directory environment in my project.

<img width="363" alt="Launching Active Directory Users and Computers (ADUC)" src="https://github.com/user-attachments/assets/9da562e1-18e3-4b3d-9307-d171f8db3e94">

## Creating a New Organizational Unit (OU)

In this step, I created a new **Organizational Unit (OU)** called **“Students”** within the **THM** domain in Active Directory. OUs are containers used to organize and manage users, computers, and other objects in the directory. They help administrators apply policies and manage permissions more efficiently by grouping objects with similar administrative needs.

<img width="745" alt="Creating a New Organizational Unit (OU)" src="https://github.com/user-attachments/assets/ef6372ac-edc4-44a4-8a0c-2e00cfb7acbf">

## Configuring User Account Properties

In this step, I configured the properties for a user account named **Bob** in the **THM** domain. The window shows various account settings, such as login details and password policies.

<img width="745" alt="Configuring User Account Properties" src="https://github.com/user-attachments/assets/9079c1a8-b464-4991-af30-65a4d3143293">

## Attempting to Delete an Organizational Unit (OU)

In this step, I attempted to delete the **Research and Development** Organizational Unit (OU) in Active Directory but received an error message.

• This error message highlights possible reason why the OU cannot be deleted:

**Protected from Accidental Deletion**: The OU has an additional protection setting that prevents accidental deletion. This setting can be toggled off by modifying the OU’s properties and unchecking the **“Protect object from accidental deletion”** option.

<img width="748" alt="Protected from Accidental Deletion" src="https://github.com/user-attachments/assets/552f8d0d-705f-482f-83d6-70063e4898a4">

## Enabling Advanced Features in Active Directory

In this step, I enabled **Advanced Features** in the **Active Directory Users and Computers (ADUC)** console.

• Enabling **Advanced Features** allows administrators to access additional options and settings within ADUC, such as advanced security properties, the **Object** tab, and the ability to modify objects protected from accidental deletion.

• This is necessary to make more granular changes to AD objects, such as disabling the accidental deletion protection on Organizational Units (OUs), which was preventing the deletion of the **Research and Development** OU in the previous task.

<img width="745" alt="Enabling Advanced Features in Active Directory" src="https://github.com/user-attachments/assets/382440a6-d66f-4901-8eed-a623b4479467">

In this case, I needed to access the properties of the OU to resolve the issue from the previous steps, where I was blocked from deleting the OU due to protection settings.

<img width="743" alt="Enabling Advanced Features in Active Directory" src="https://github.com/user-attachments/assets/8d4bee06-8109-4fba-b7b2-36eaac435744">

In this step, I accessed the **Research and Development** OU’s properties and unchecked the **“Protect object from accidental deletion”** option under the **Object** tab.

<img width="740" alt="Enabling Advanced Features in Active Directory" src="https://github.com/user-attachments/assets/b47dae7a-757b-44c5-8e74-181dd4425993">

The confirmation prompt ensures that I am aware the OU contains other objects, such as users or groups, and that deleting it will also remove all those contained objects.

<img width="748" alt="Enabling Advanced Features in Active Directory" src="https://github.com/user-attachments/assets/ceac8d14-bb5f-4715-b703-6fb8e34bf994">

## Delegating Control Over the Sales OU

In this step, I initiated the process to delegate control over the **Sales** Organizational Unit (OU) by selecting the **Delegate Control** option from the right-click menu.

**Purpose**:

• **Delegating control** allows a user or group to perform specific administrative tasks within the designated OU without granting them full administrative rights.

• This delegation is often used to provide limited administrative rights to IT staff, such as allowing them to reset passwords for users within the Sales department.

<img width="744" alt="Enabling Advanced Features in Active Directory" src="https://github.com/user-attachments/assets/8c9abc2b-3f10-4d79-908d-6ef14d4b343a">

**The Delegation of Control Wizard** is used to delegate specific administrative tasks (e.g., resetting passwords) to non-administrators. This can be useful for distributing administrative responsibilities to support staff without giving them full administrative rights.

<img width="740" alt="The Delegation of Control Wizard" src="https://github.com/user-attachments/assets/ebdbdc65-cf9b-4d61-b33d-ebb1d23143da">

In this step, I selected the user **Phillip** in the **Delegation of Control Wizard** to delegate specific administrative rights. By typing “phillip” and using the **Check Names** function, I ensured that I was selecting the correct user from the Active Directory.

<img width="742" alt="Delegation of Control Wizard" src="https://github.com/user-attachments/assets/cd24ccab-8543-4b71-8b48-da5e74280151">

<img width="737" alt="Delegation of Control Wizard" src="https://github.com/user-attachments/assets/d629e1fe-207f-45d9-a749-658849163685">

<img width="737" alt="Delegation of Control Wizard" src="https://github.com/user-attachments/assets/57beb239-24a9-43e2-a3c7-bf41799c6f41">

**Delegating the Task of Resetting User Passwords**

In this step, I used the **Delegation of Control Wizard** to assign Phillip the task of **Resetting user passwords and forcing a password change at the next logon**. This specific delegation allows Phillip to reset passwords for users in the domain and ensure that users must change their password when they log in again.

<img width="497" alt="Delegation of Control Wizard" src="https://github.com/user-attachments/assets/3b82a1b9-fc54-4de1-93c9-8bc786bf4a3e">

<img width="497" alt="Delegation of Control Wizard" src="https://github.com/user-attachments/assets/2f63b1bb-daea-4065-adc2-4c500c8ea034">

## Remote Desktop Connection

• I initiated a Remote Desktop Connection (RDP) to remotely access a machine in the THM domain. I entered the IP address of the machine and prepared to connect as a specified user to perform management tasks. The warning about the remote computer’s identity was displayed because the machine’s identity couldn’t be verified, but I proceeded as it was a known, trusted connection within the domain.

**Logging in as Phillip**

• Once connected via RDP, I logged into the machine using the domain credentials for the user ‘phillip’. This step was essential to access privileges assigned to this user, including the delegated ability to reset passwords within the domain. I ensured I logged in with the correct domain, “THM”, to perform the necessary administrative tasks.

<img width="414" alt="Logging in as Phillip" src="https://github.com/user-attachments/assets/64fef5e8-9bf6-4c1f-8fa9-a6bf98f043ae">

<img width="476" alt="Logging in as Phillip" src="https://github.com/user-attachments/assets/e744a16d-28e1-45c7-a0c0-bcc59e204b52">

**Resetting the Password for a User**: In the screenshot, I attempted to use the command Set-ADAccountPassword to reset the password for the user Sophie. However, the password I provided did not meet the **domain’s password complexity requirements**, which resulted in an error. This error highlighted that Active Directory has policies regarding the length, complexity, and history of passwords, ensuring security across the domain.

<img width="711" alt="Resetting the Password for a User" src="https://github.com/user-attachments/assets/008e2d03-a956-4730-8d35-2f324d8863c0">

**Password Reset**:

• I used the Set-ADAccountPassword command to reset Sophie’s password to “ComplexPass123!” and successfully executed the operation, as shown in the first part of the output. This password now meets the complexity requirements of the domain.

**Forcing Password Change**:

• The Set-ADUser -ChangePasswordAtLogon $true command was used to ensure that Sophie will be prompted to change her password the next time she logs in. This enhances security by ensuring she sets a new, private password.

**Verifying User Properties**:

• I ran the Get-ADUser command to retrieve properties for Sophie, including checking if her password had been set and expired. This confirms that the password change process has been successfully applied.

<img width="719" alt="Verifying User Properties" src="https://github.com/user-attachments/assets/e8631e09-fa17-47d9-a198-98f5cf0d5fc3">

**Logging in as Sophie and Changing the Password**:

• When Sophie attempted to log in, the system immediately prompted a password change. The first screenshot shows the message: “The user’s password must be changed before signing in.”

• Once Sophie entered the new password, the second screenshot shows confirmation that her password had been successfully changed, allowing her access to the system.

<img width="451" alt="Logging in as Sophie and Changing the Password" src="https://github.com/user-attachments/assets/33f04f0a-40d3-4aea-8836-56a2997f1c56">

<img width="401" alt="Logging in as Sophie and Changing the Password" src="https://github.com/user-attachments/assets/001a7fba-97d8-42b9-af94-1d99e5eae564">

**Managing Organizational Units (OUs) and Computer Objects in Active Directory**

In this part of the project, I worked with **Active Directory Users and Computers** to manage and organize various computer objects within the domain.

The goal was to structure the devices in different **Organizational Units (OUs)** based on their roles for easier policy management.

As part of restructuring, I moved multiple computer objects (e.g., **LPT-SOPHIE**, **PC-CLAIRE**, **PC-MARK**) into the **Workstations** OU to group them appropriately.

• The system provided a warning message, as seen in the screenshot, about potential changes in how group policies are applied once objects are moved between OUs. This ensures that moving objects doesn’t inadvertently affect system performance or policy application.

<img width="689" alt="Managing Organizational Units (OUs) and Computer Objects in Active Directory" src="https://github.com/user-attachments/assets/951e8fe8-6882-453f-b810-e38066f13a45">

**Managing Group Policy Objects (GPOs) in Active Directory**

In this section of the project, I used the **Group Policy Management** console to manage and configure **Group Policy Objects (GPOs)** within the thm.local domain.

The aim was to verify and manage the existing GPOs that control various aspects of user and computer behavior within the domain.

<img width="687" alt="Managing Group Policy Objects (GPOs) in Active Directory" src="https://github.com/user-attachments/assets/822bcf0e-fb2e-478d-8e99-0a5c5f323a38">

**Creating and Linking Group Policy Objects (GPOs) in Active Directory**

As part of the project, I worked on creating a new **Group Policy Object (GPO)** and linking it to the domain in **Active Directory** to implement specific policies for devices and users.

By creating and linking a custom GPO, I ensured that specific security configurations and policies would be enforced across the domain. This allows centralized control over user and device behavior, ensuring compliance with organizational security standards.

<img width="691" alt="Creating and Linking Group Policy Objects (GPOs) in Active Directory" src="https://github.com/user-attachments/assets/7c6bdc71-2576-41d0-b43b-ae7892797908">

**Configuring User Account Policies in Group Policy**

In this part of the project, I configured specific user account settings within a **Group Policy Object (GPO)** using the **Group Policy Management Editor**.

By enforcing this policy, I ensured that all users within the domain would have a standardized account picture, contributing to a more uniform environment and simplifying administrative tasks related to user account management.

<img width="786" alt="Configuring User Account Policies in Group Policy" src="https://github.com/user-attachments/assets/194fcce2-2c78-4f0b-bbcb-5a402160f2d2">

**Configuring Control Panel Settings in Group Policy**

In this phase of the project, I worked on configuring the **Control Panel** settings under **User Configuration** within a Group Policy Object (GPO) using the **Group Policy Management Editor**.

By configuring Control Panel settings, I was able to limit user access to sensitive system settings, reducing the risk of unauthorized modifications and enhancing the overall security posture of the system.

I enforced the **Prohibit access to Control Panel and PC settings** policy to prevent users from accessing and modifying critical system settings.

<img width="788" alt="Configuring Control Panel Settings in Group Policy" src="https://github.com/user-attachments/assets/339757dc-bcd4-4892-92ed-da61d4fb9cf0">

<img width="784" alt="Configuring Control Panel Settings in Group Policy" src="https://github.com/user-attachments/assets/e618ae7f-6090-406b-b7aa-268dded58ad2">

<img width="787" alt="Configuring Control Panel Settings in Group Policy" src="https://github.com/user-attachments/assets/7f277e7d-dc25-4480-b9bf-a5dfc988a65f">

<img width="680" alt="Configuring Control Panel Settings in Group Policy" src="https://github.com/user-attachments/assets/6d78ed41-4ef2-4b87-8dbc-7db4459ae9e7">

**Linking the ‘Restrict Control Panel Access’ GPO to THM Organizational Unit (OU)**

In this step, I linked the **Restrict Control Panel Access** Group Policy Object (GPO) to the **THM** Organizational Unit (OU), ensuring that the policy is applied to all users and devices within that specific organizational structure.

<img width="627" alt="Restrict Control Panel Access" src="https://github.com/user-attachments/assets/e4ba21d5-6044-404c-bb70-1e9e22e2685b">

<img width="627" alt="Restrict Control Panel Access" src="https://github.com/user-attachments/assets/d5b2b67f-1510-4afe-814a-85f236c0098d">

I added a specific user to the scope of the **Restrict Control Panel Access** Group Policy Object (GPO) to ensure the policy applies only to the intended users.

<img width="627" alt="Restrict Control Panel Access" src="https://github.com/user-attachments/assets/aa202aed-2f10-4426-aaaf-b03f99d645bc">

<img width="626" alt="Restrict Control Panel Access" src="https://github.com/user-attachments/assets/887737c2-6572-40f7-8b44-e4440f9acbba">

By linking the **Restrict Control Panel Access** GPO to multiple OUs and applying it to specific users, I ensured that the policy is enforced across targeted areas of the organization. This granular control allows for flexible management of security settings based on the organizational structure and individual user requirements.

This section captures the detailed process of linking the GPO to specific OUs and filtering the policy by user.

**Forcing a Group Policy Update with PowerShell**

In this step, I used **PowerShell** to force a **Group Policy Update** across the system. By using the gpupdate /force command, I successfully ensured that all Group Policy configurations were immediately applied across the domain. This method is especially useful for testing new policies and ensuring immediate enforcement after making changes.

<img width="623" alt="Forcing a Group Policy Update with PowerShell" src="https://github.com/user-attachments/assets/f325e547-9ade-4d88-b430-43870f447e2c">

**Modifying the Default Domain Policy in Group Policy Management**

In this phase of the project, I accessed and modified the **Default Domain Policy** to enforce security settings across the domain.

The goal was to modify the **Default Domain Policy** to ensure consistent security configurations across all users and computers within the domain.

<img width="820" alt="Default Domain Policy" src="https://github.com/user-attachments/assets/c8afa869-ad9e-45d5-a6fd-e7cf2939ac42">

**Configuring Password Policies in Group Policy**

In this part of the project, I configured the **Password Policy** settings within the **Default Domain Policy** to enforce secure password practices for all users in the domain.

I configured the **Minimum Password Length** policy to enforce a higher level of password security across the domain.

<img width="787" alt="Minimum Password Length" src="https://github.com/user-attachments/assets/c3455d20-65d6-413c-8606-2c376f52752c">

<img width="784" alt="Minimum Password Length" src="https://github.com/user-attachments/assets/1ebd9d82-8836-4285-b8a2-592903c32f92">

**Creating the Auto Lock Screen Group Policy Object (GPO)**

By creating and configuring the **Auto Lock Screen** GPO, I ensured that unattended systems are automatically locked after a period of inactivity, reducing the risk of unauthorized access. This policy helps enforce security best practices and protects sensitive information by securing idle systems.

<img width="626" alt="Auto Lock Screen" src="https://github.com/user-attachments/assets/3475bfaa-fb98-422e-9639-cae058f0f00f">

**Configuring the Auto Lock Screen Group Policy**

In this phase of the project, I configured the **Auto Lock Screen** GPO to automatically lock user screens after a period of inactivity. This enhances security by ensuring that unattended systems are secured.

To configure the **Auto Lock Screen** policy to automatically lock the screen after 300 seconds (5 minutes) of inactivity, thereby protecting systems from unauthorized access when left idle.

**Steps Taken:**

**Editing the Auto Lock Screen GPO:**

• In the **Group Policy Management** console, I right-clicked on the newly created **Auto Lock Screen** GPO and selected **Edit…** to open the **Group Policy Management Editor**. This allowed me to configure the policy settings, as shown in the first screenshot.

<img width="635" alt="Group Policy Management" src="https://github.com/user-attachments/assets/25659f46-cae5-4e96-b731-838266d0f454">

**Navigating to Security Options:**

• I navigated to **Computer Configuration** > **Policies** > **Windows Settings** > **Security Settings** > **Local Policies** > **Security Options**, as shown in the second screenshot.

• This section contains policies that govern security-related behaviors for Windows machines, including settings that can control automatic screen locking.

<img width="625" alt="Navigating to Security Options" src="https://github.com/user-attachments/assets/88c7bef9-c617-43ec-8892-4c5b42cd376e">

**Configuring the Inactivity Limit:**

• I selected **Interactive logon: Machine inactivity limit**, which is the policy that controls how long the system remains idle before it locks the screen. In the third screenshot, you can see this policy highlighted in the **Security Options** section.

• I enabled the policy and set the inactivity limit to **300 seconds (5 minutes)**, as shown in the final screenshot. This ensures that the screen will lock after 5 minutes of user inactivity, requiring reauthentication to unlock the machine.

<img width="622" alt="Configuring the Inactivity Limit" src="https://github.com/user-attachments/assets/1d8551b2-d435-472e-96d5-e94295ca31a5">

<img width="623" alt="Configuring the Inactivity Limit" src="https://github.com/user-attachments/assets/a5cd95dc-ab35-4ac8-bf30-78b7daf867aa">

**Applying the Policy:**

• After configuring the settings, I clicked **Apply** and **OK** to ensure the changes were saved. This step guarantees that the inactivity limit is enforced across all systems where the **Auto Lock Screen** GPO is applied.

• I then performed a gpupdate /force to apply the new GPO settings immediately, ensuring that the policy takes effect without waiting for the next scheduled refresh.

**Testing the Policy:**

• To verify the effectiveness of the new policy, I left a test system idle for 5 minutes and confirmed that the screen locked automatically after the set inactivity period. This confirmed that the policy was working as intended.

<img width="623" alt="Testing the Policy" src="https://github.com/user-attachments/assets/64d7b65d-5737-4856-9c8a-53d66fe9e4ca">

**Linking the Auto Lock Screen GPO to the THM Organizational Unit**

In this step, I linked the **Auto Lock Screen** Group Policy Object (GPO) to the **THM** Organizational Unit (OU), ensuring that the policy applies to all users and computers within the specified OU.

<img width="636" alt="Linking the Auto Lock Screen GPO to the THM Organizational Unit" src="https://github.com/user-attachments/assets/7c17b83d-2753-432b-bce4-53fead721ab9">

<img width="639" alt="Linking the Auto Lock Screen GPO to the THM Organizational Unit" src="https://github.com/user-attachments/assets/83055a23-fd0f-4dcd-a6d2-ad0e7da5c592">

**Finalizing the Auto Lock Screen GPO: Linking and Enforcing Policies for Specific Users and OUs**

To enforce the **Auto Lock Screen** GPO across the **THM** OU, applying it to all authenticated users as well as the specific user **Mark (mark@thm.local)**, and ensure the policy’s enforcement across organizational units.

<img width="623" alt="Finalizing the Auto Lock Screen GPO: Linking and Enforcing Policies for Specific Users and OUs" src="https://github.com/user-attachments/assets/4df64570-0776-44ec-9747-d4a6ed1a61ac">

<img width="732" alt="Finalizing the Auto Lock Screen GPO: Linking and Enforcing Policies for Specific Users and OUs" src="https://github.com/user-attachments/assets/e10421d6-e70b-4451-a037-57415b074983">

## Conclusion

This project demonstrated the implementation of centralized management in a Windows Domain environment using **Active Directory** and **Group Policy Objects**. By effectively managing users, devices, and security policies from a central location, the project showcases how such an environment can enhance security, scalability, and operational efficiency across an organization.



## Contributing

We welcome contributions from the community. If you have any suggestions, bug reports, or feature requests, please open an issue or submit a pull request. 

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any inquiries or further information, please contact me at [martaa.dominik@gmail.com](mailto:martaa.dominik@gmail.com).

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/marta-dominik-a67803233/)
