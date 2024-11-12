# Windows Domain Setup and Administration

In this project, I demonstrated the process of setting up and administering a **Windows Domain** environment, showcasing key network administration and security management skills. The project covered important aspects such as user account creation, device management, security policy implementation, and central control using **Active Directory** and **Group Policy Objects (GPOs)**.

## Key Areas Covered

- **Windows Domain Setup and Configuration**: Establishing a centralized network environment using **Active Directory** to manage resources, users, and devices efficiently.
- **User Account and Device Management**: Creating, managing, and organizing users and computers in **Organizational Units (OUs)** within Active Directory for better control and management.
- **Security and Permissions**: Implementing security policies, such as password policies and user access controls, to maintain a secure environment. This included enforcing password complexity requirements and restricting user access to sensitive system settings like the **Control Panel**.
- **Scalability and Efficiency**: Demonstrating how centralized management simplifies network operations for hundreds of users and devices across multiple locations, reducing manual configurations and enhancing administrative efficiency.

## Key Steps and Configurations

### Launching Active Directory Users and Computers (ADUC)
In this step, I opened the **Active Directory Users and Computers (ADUC)** tool from the Windows Start menu. ADUC is the central interface for managing the directory services provided by **Active Directory**. It allows administrators to create, modify, and manage users, computers, and other objects within a domain.

![Launching ADUC](https://prod-files-secure.s3.us-west-2.amazonaws.com/b7cbf48a-0265-453d-8d27-f73b88827615/a89033d6-54e5-4d93-9f81-19b21fc5277c/Screenshot_2024-10-22_at_08.31.31.png)

### Creating a New Organizational Unit (OU)
Created a new **Organizational Unit (OU)** named **"Students"** within the **THM** domain. OUs help administrators apply policies and manage permissions efficiently by grouping objects with similar administrative needs.

![Creating OU](https://prod-files-secure.s3.us-west-2.amazonaws.com/b7cbf48a-0265-453d-8d27-f73b88827615/bb845bc0-4e5e-48d8-8b46-a5349ce50f91/Screenshot_2024-10-22_at_08.37.43.png)

### Configuring User Account Properties
Configured properties for a user account named **Bob** in the **THM** domain, setting up login details and password policies.

![Configuring User Properties](https://prod-files-secure.s3.us-west-2.amazonaws.com/b7cbf48a-0265-453d-8d27-f73b88827615/0ecb3123-95dc-4d42-babc-537443516851/Screenshot_2024-10-22_at_08.39.06.png)

### Attempting to Delete an Organizational Unit (OU)
Attempted to delete the **Research and Development** OU but received an error due to accidental deletion protection. This was resolved by unchecking the **"Protect object from accidental deletion"** option.

![Deleting OU](https://prod-files-secure.s3.us-west-2.amazonaws.com/b7cbf48a-0265-453d-8d27-f73b88827615/6804270c-e85c-4a77-aca9-e69a17e9cb5a/Screenshot_2024-10-22_at_08.51.57.png)

### Delegating Control Over the Sales OU
Used the **Delegation of Control Wizard** to delegate the task of resetting passwords within the **Sales** OU to user **Phillip**.

![Delegating Control](https://prod-files-secure.s3.us-west-2.amazonaws.com/b7cbf48a-0265-453d-8d27-f73b88827615/46ce017a-668c-45a3-8593-a10a07ba4b2a/Screenshot_2024-10-22_at_08.57.08.png)

### Remote Desktop Connection and Logging in as Phillip
Connected via RDP as **Phillip** to verify delegated permissions and reset user passwords as needed.

![Logging in as Phillip](https://prod-files-secure.s3.us-west-2.amazonaws.com/b7cbf48a-0265-453d-8d27-f73b88827615/e4856335-a2d6-4a9b-9d8d-52c15b398347/Screenshot_2024-10-22_at_09.30.38.png)

### Resetting the Password for a User
Attempted to reset the password for **Sophie** to meet domain complexity requirements and forced a password change at her next login.

![Password Reset](https://prod-files-secure.s3.us-west-2.amazonaws.com/b7cbf48a-0265-453d-8d27-f73b88827615/07d80b1c-ac18-4d40-bfca-16b6b6a7d042/Screenshot_2024-10-22_at_10.39.16.png)

### Managing Organizational Units (OUs) and Computer Objects
Organized computer objects by moving them to the **Workstations** OU, optimizing group policy application.

![Managing OUs](https://prod-files-secure.s3.us-west-2.amazonaws.com/b7cbf48a-0265-453d-8d27-f73b88827615/6000fe26-7eb8-40ce-8397-ad77f6bb8144/Screenshot_2024-10-22_at_20.03.10.png)

### Managing and Linking Group Policy Objects (GPOs)
Created, linked, and configured **Group Policy Objects (GPOs)** to enforce domain policies, such as restricting Control Panel access.

![GPO Management](https://prod-files-secure.s3.us-west-2.amazonaws.com/b7cbf48a-0265-453d-8d27-f73b88827615/91f0ed5b-0918-4697-b17d-3df9a62ddc62/Screenshot_2024-10-22_at_20.07.07.png)

### Configuring Control Panel Access Policy
Set up a **Control Panel restriction policy** to prohibit unauthorized changes, enhancing security.

![Restrict Control Panel](https://prod-files-secure.s3.us-west-2.amazonaws.com/b7cbf48a-0265-453d-8d27-f73b88827615/ec6a9738-4c2b-473f-8d62-46086cb0e5e2/Screenshot_2024-10-22_at_20.16.57.png)

### Enforcing Password Policies
Configured the **Default Domain Policy** to enforce a minimum password length and complexity, promoting secure password practices across the domain.

![Password Policy](https://prod-files-secure.s3.us-west-2.amazonaws.com/b7cbf48a-0265-453d-8d27-f73b88827615/90a7d3ef-b91b-4d95-8547-a94cb9efbfa4/Screenshot_2024-10-23_at_07.55.48.png)

### Auto Lock Screen Policy
Created the **Auto Lock Screen** GPO to automatically lock screens after 5 minutes of inactivity, reducing the risk of unauthorized access.

![Auto Lock Screen](https://prod-files-secure.s3.us-west-2.amazonaws.com/b7cbf48a-0265-453d-8d27-f73b88827615/b6632753-1af7-4bae-a409-f509067ddafe/Screenshot_2024-10-23_at_09.55.49.png)

## Finalizing and Applying Policies
Linked the **Auto Lock Screen** GPO to the **THM** OU and confirmed policy enforcement across specific users and OUs.

![Finalizing Policies](https://prod-files-secure.s3.us-west-2.amazonaws.com/b7cbf48a-0265-453d-8d27-f73b88827615/6b222668-ee87-4fe9-ad5b-f262d689dc7f/Screenshot_2024-10-23_at_10.38.00.png)

## Conclusion
This project demonstrated the implementation of centralized management in a Windows Domain environment using **Active Directory** and **Group Policy Objects**. By effectively managing users, devices, and security policies from a central location, the project showcases how such an environment can enhance security, scalability, and operational efficiency across an organization.


## Contributing

We welcome contributions from the community. If you have any suggestions, bug reports, or feature requests, please open an issue or submit a pull request. 

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any inquiries or further information, please contact me at [martaa.dominik@gmail.com](mailto:martaa.dominik@gmail.com).

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/marta-dominik-a67803233/)
