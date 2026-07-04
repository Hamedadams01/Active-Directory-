# Organizational Units, Users, and Groups

## Overview

Building out the Active Directory structure on Houtech: a departmental OU hierarchy, user accounts, and security groups to mirror a real company environment.

## Objectives


- Design a top-level OU to house all departmental sub-OUs
- Create OUs for each department to organize users, groups, and future Group Policy settings
- Create individual user accounts within their department's OU
- Create a security group per department and populate it with that department's users
- Verify account and group membership accuracy throughout


## Process

1. Creating the Top-Level OU

Opened Active Directory Users and Computers on Houtech, right-clicked the domain (Houtech.local), and selected New > Organizational Unit. The dialog defaults to "Protect container from accidental deletion" checked.

![image alt](https://github.com/Hamedadams01/Active-Directory-/blob/main/Screenshot%202026-06-21%20105236.png?raw=true)

2. Naming the Top-Level OU

Named the new OU Department and unchecked "Protect container from accidental deletion" so it could be freely modified while the structure was still being built out.

![image alt](https://github.com/Hamedadams01/Active-Directory-/blob/main/Screenshot%202026-06-21%20105300.png?raw=true)

3. Building the Department Sub-OUs

Inside the Department OU, six Department OUs were created: Human Resources (HR), Finance Department, Marketing Department, Information Technology, Sales Department, and Management.

![image alt](https://github.com/Hamedadams01/Active-Directory-/blob/main/Screenshot%202026-06-21%20105936.png?raw=true)

4. Creating a User in the HR OU

Right-clicked the Human Resources (HR) OU and used New > User to open the user creation wizard, building the account inside Houtech.local/Department/Human Resources(HR).
![image alt](https://github.com/Hamedadams01/Active-Directory-/blob/main/Screenshot%202026-06-21%20105950.png?raw=true
)
5. Setting the Account Password

On the next screen, set and confirmed the account password and left "User must change password at next logon" checked, following standard account provisioning practice.

![image alt](https://github.com/Hamedadams01/Active-Directory-/blob/main/Screenshot%202026-06-21%20110046.png?raw=true)

6. Repeating for Additional HR Users

Repeated the New User wizard for additional accounts (e.g., Emily Garcia), each auto-populating a logon name based on first initial + last name.

![image alt](https://github.com/Hamedadams01/Active-Directory-/blob/main/Screenshot%202026-07-01%20100955.png?raw=true)


7. Confirming HR User Accounts

Verified the Human Resources OU now contained four user accounts, confirming each was created successfully before moving on to grouping.

![image alt](https://github.com/Hamedadams01/Active-Directory-/blob/main/Screenshot%202026-06-21%20110358.png?raw=true)

8. Creating the Department Security Group

Right-clicked the HR OU and used New > Group to create #Human_Resources, with group scope set to Global and group type set to Security — a single group to manage permissions and policies for the whole department.

![image alt](https://github.com/Hamedadams01/Active-Directory-/blob/main/Screenshot%202026-06-21%20113557.png?raw=true)

9. Reviewing a User's Account Properties

Opened an HR user's (David Smith's) account properties on the General tab to confirm first name, last name, and display name were all set correctly.

![image alt](https://github.com/Hamedadams01/Active-Directory-/blob/main/Screenshot%202026-06-21%20113646.png?raw=true)

10. Checking Starting Group Membership

Checked the Member Of tab and confirmed the account was currently only a member of the default Domain Users group, which was also set as the primary group.

![image alt](https://github.com/Hamedadams01/Active-Directory-/blob/main/Screenshot%202026-06-21%20113651.png?raw=true)

11. Adding the User to the Department Group

Clicked Add on the Member Of tab, opened the Select Groups dialog, and entered #Human_Resources to link the account to its department's security group.

![image alt](https://github.com/Hamedadams01/Active-Directory-/blob/main/Screenshot%202026-06-21%20113700.png?raw=true)

12. Verifying Group Membership

Opened the #Human_Resources group properties and checked the Members tab, confirming all four HR user accounts were listed.
![image alt](https://github.com/Hamedadams01/Active-Directory-/blob/main/Screenshot%202026-06-21%20113813.png?raw=true
)
13. Repeating Across Departments

Repeated the same OU, user, and group workflow for the Sales Department, then verified the #Sales_Department group's Members tab listed all nine Sales users — confirming the process was repeatable and consistent across departments.
![image alt](https://github.com/Hamedadams01/Active-Directory-/blob/main/Screenshot%202026-06-21%20115241.png?raw=true)
