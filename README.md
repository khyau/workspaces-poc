# workspaces-poc

> Tested in
> * ap-southeast-1
> * should work in other service available region

# First Step: Create the WorkSpaces Lab VPC network infrastructure using AWS CloudFormation 
The steps in this section will walk you through running an AWS CloudFormation script to build out a fully functioning Virtual Private Cloud (VPC) infrastructure in the selected region you choose under your AWS account in an automated fashion.

| Components | Value |
| ------------- | ------------- |
| VPC Name  | WorkSpaces VPC  |
| VPC IPv4 CIDR block   | 10.X.0.0/16   Where X is your choice (0-255)  |
| Public subnet name  | WorkSpaces Public Subnet  |
| Public subnet IPv4 CIDR  | 10.X.0.0/24  (Where X is the value you choose for the VPC CIDR above)  |
| Private subnet 1 name | WorkSpaces Private Subnet1 |
| Private subnet 1 IPv4 CIDR | 10.X.1.0/24   (Where X is the value you choose for the VPC CIDR above) |
| Private subnet 2 name | WorkSpaces Private Subnet2 |
| Private subnet 2 IPv4 CIDR | 10.X.2.0/24   (Where X is the value you choose for the VPC CIDR above] |
| Internet Gateway Name |	WorkSpaces IGW  |
| NAT Gateway |	WorkSpaces NatGateway  |
| WorkSpaces Public Route Table |	FYI-Routes Public subnet internet traffic to the Internet Gateway. |
| WorkSpaces Private Route Table |	FYI-Routes Private subnet internet traffic to the NAT Gateway.  |


![workspaces-poc](images/network_diagram.jpg)


# Second Step: Create an AWS Directory Service
Amazon WorkSpaces requires an AWS Directory Service store to facilitate WorkSpace and user information for authentication and management purposes. The Amazon WorkSpaces managed service can create this directory in the cloud for you using either Simple AD  or AWS Managed Microsoft AD. Additionally, you can connect to an existing Active Directory using the Active Directory Connector (or AWS Managed Microsoft AD via a standard domain trust) through the AWS Directory Services console. 
