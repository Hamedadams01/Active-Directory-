# Active-Directory 
Active Directory — OU, User, and Group Structure
Overview
With the domain controller in place, this project builds the actual organizational structure inside Active Directory — a department-based OU hierarchy, individual user accounts within each department, and security groups used to manage permissions collectively rather than per-user. This structure is the backbone that later GPOs, shared folders, and helpdesk scenarios all attach to.
# Objectives

- Design a realistic, department-based OU hierarchy under the domain root
- Populate each department OU with individual user accounts
- Create security groups per department to centralize permission management
- Verify user-to-group membership is accurate before relying on it elsewhere
- Confirm the workflow is repeatable and consistent across multiple departments
# Step-by-Step

- I opened Active Directory Users and Computers and right-clicked the Houtech.local domain to create a new top-level "Department" OU, unchecking "Protect container from accidental deletion" so I could still edit it easily during testing.

![image alt]()

- I created six child OUs under Department: Human Resources (HR), Finance Department, Marketing Department, Information Technology, Sales Department, and Management — mirroring a realistic company structure.

![image alt]()

- I right-clicked the HR OU and chose New > User to start creating accounts inside Houtech.local/Department/Human Resources(HR).

![image alt]()

- I entered and confirmed a password for the account, leaving "User must change password at next logon" checked to follow standard provisioning practice.

![image alt]()

- I repeated this process to create four HR accounts: James Carter, Micheal Johnson, Emily Garcia, and David Smith.

![image alt]()

- I right-clicked the HR OU again and chose New > Group to create #Human_Resources, setting the scope to Global and the type to Security.

![image alt]()

- I opened David Smith's properties to confirm his General tab details were correct before adding him to a group.

![image alt]()

- I checked David Smith's Member Of tab and confirmed he only belonged to the default Domain Users group.

![image alt]()

- I clicked Add on the Member Of tab and typed "#Human_Resources" to add David Smith to the HR security group.

![image alt]()

- I opened the #Human_Resources group's Members tab and confirmed all four HR users were listed correctly.

![image alt]()

- I repeated the same OU, user, and group process for the Sales Department, creating nine users (Gabriel Evans, Luke Carter, Owen Mitchell, Henry Perez, Adrian Ross, Benjamin Allen, Jonathan Walker, Samuel Hall, and Jacob Adams).

![image alt]()

-I opened the #Sales_Department group's Members tab and confirmed all nine Sales users were listed, verifying the workflow was repeatable across departments.

![image alt]()

# Conclusion

- A clean, six-department OU hierarchy was built under Houtech.local
- User accounts were provisioned correctly within their respective department OUs
- Security groups were created and verified for HR and Sales, with membership confirmed for both
- This structure is ready to support Group Policy application and permission management by department
