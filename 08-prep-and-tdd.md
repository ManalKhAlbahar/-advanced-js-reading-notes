# Read08
* Answer the question.
* RBAC tutorial.
* 5 steps to RBAC.
* wiki - RBAC.

### *Answer the question*
- Q1 : The basis Auth allow you to access the API directly with your credential : user/password. Used case
The use case for this are integration with reporting tools like PowerBI, Tableau, QLik, BoldBI.
Bearer Token :It is the recommended Authentication methods whenever possible. It is ideal when scripting, when 
developing external app or when doing integration with external tools.

- Q2 : A JSON web token (JWT) is JSON Object which is used to securely transfer information over the web (between two parties). It can be used for an authentication system and can also be used for information exchange.

- Q3: 
-  Never store unencrypted secrets in .git repositories
-  Add sensitive files in .gitignore .
- Don’t share your secrets unencrypted in messaging systems like slack.

### *RBAC tutorial*
RBIC (Role-Based Access Control), also known as role-based security, is an access control method that assigns 
permissions to end-users based on their role within your organization. 

For more details watch this [RBAC tutorial](https://www.youtube.com/watch?v=C4NP8Eon3cA).

### *5 steps to RBAC*
- RBAC is the idea of assigning system access to users based on their role within an organization. The system 
needs of a given workforce are analyzed, with users grouped into roles based on common job responsibilities and 
system access needs.
- Benefits of RBAC: the assignment of access rights becomes systematic and repeatable. Further, it is much easier 
to audit user rights, and to correct any issues identified.
- Five steps to simple RBAC :
- 1- Inventory your systems.
- 2- Analyze your workforce and create roles.
- 3- Assign people to roles.
- 4- Never make one-off changes
- 5- Audit

For more details see [5 steps to RBAC](https://www.csoonline.com/article/3060780/5-steps-to-simple-role-based-access-control.html).

### *wiki - RBAC*
role-based access control (RBAC) or role-based security: is an approach to restricting system access to authorized 
users. It is an approach to implement mandatory access control (MAC) or discretionary access control (DAC).
- Three primary rules are defined for RBAC:
- 1- Role assignment: A subject can exercise a permission only if the subject has selected or been assigned a role.
- 2- Role authorization: A subject's active role must be authorized for the subject. With rule 1 above, this rule 
ensures that users can take on only roles for which they are authorized.
- 3- Permission authorization: A subject can exercise a permission only if the permission is authorized for the 
subject's active role. With rules 1 and 2, this rule ensures that users can exercise only permissions for which 
they are authorized.

For more details see [wiki - RBAC](https://en.wikipedia.org/wiki/Role-based_access_control).