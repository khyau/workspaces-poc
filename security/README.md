# WorkSpaces Security

As part of the shared responsibility model, security is a shared responsibility between Amazon Web Services (AWS) and you. AWS is responsible for protecting the infrastructure that runs the AWS services while you are responsible for securing your data in AWS through appropriate permissions and WorkSpace management as outlined in the Best Practices for Deploying Amazon WorkSpaces whitepaper. 

# Before start
*Define User Group*
How you define your user groups should reflect how you classify your data and the access controls associated with the classifications. A common approach is to begin by separating your internal (employees) and external (vendors and consultants) users. The identification process also helps to ensure that you’re following the principle of least privilege by limiting access to certain applications or resources. These user groups are the building blocks for designing the rest of your security controls, including the directories, access controls, and security groups.

![workspaces-poc](images/ou.png)

*Configure Active Directory*
mazon Workspaces can create and manage a directory for you so that users are entered into that directory when you provision a WorkSpace. As an alternative, you can integrate WorkSpaces with an existing, on-premises Microsoft Active Directory (AD) so your users can use the credentials they already know to access applications.

Within Amazon WorkSpaces, directories play a large part in how access to workspaces is configured. Directories within Amazon WorkSpaces are used to store and manage information for your WorkSpaces and users. Based on the preceding two example user groups, let’s split your users’ WorkSpaces across two directories. That will help you to establish different access control settings for the two groups.
