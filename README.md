# Deploying-Virtual-Private-Cloud-with-CloudFormation
This project provides an AWS CloudFormation template to deploy a Virtual Private Cloud (VPC) with a pair of public and private subnets spread across two Availability Zones. It includes an internet gateway for public subnets and sets up the necessary routing.

## Features

- Creates a VPC with a specified CIDR block.
- Sets up public and private subnets across two Availability Zones.
- Deploys an Internet Gateway and associates it with the VPC.
- Configures route tables for public and private subnets.
- Includes a security group with no ingress rules for enhanced security.


## Prerequisites
- An AWS account.
- Necessary permissions to create and manage CloudFormation stacks, VPCs, subnets, and associated resources.
## Instructions
- Step 1: Create a New Stack:
1. Head to the AWS Management Console.
2. Navigate to the CloudFormation service.
3. Click on "Create stack" and select "With new resources (standard)".
##
- Step 2: Upload the Template:
1. In the "Create stack" page, under the "Specify template" section, choose "Upload a template file".
2. Click "Choose file" and select the create-vpc-with-cloudformation.yaml file from this repository.
3. Click "Next".

##
- Step 3: Specify Stack Details:
1. Provide a stack name (e.g., MyVPCStack).
2. Provide an environment name (e.g., Dev, Prod).

##
- Step 4: Configure Stack Options:
1. Ensure the VPC CIDR does not overlap with any existing CIDR blocks in your account.
2. Modify the default CIDR blocks for subnets if necessary.

##
- Step 5: Review and Create Stack:
1. Accept all default settings.
2. Review your configurations and click on "Create stack".



## Parameters
The following parameters can be configured in the CloudFormation template:

- EnvironmentName: An environment name that is prefixed to resource names (e.g., Dev, Prod).
- VpcCIDR: The IP range (CIDR notation) for the VPC. Default: 10.8.0.0/16.
- PublicSubnet1CIDR: The IP range (CIDR notation) for the public subnet in the first Availability Zone. Default: 10.8.10.0/24.
- PublicSubnet2CIDR: The IP range (CIDR notation) for the public subnet in the second Availability Zone. Default: 10.8.11.0/24.
- PrivateSubnet1CIDR: The IP range (CIDR notation) for the private subnet in the first Availability Zone. Default: 10.8.20.0/24.
- PrivateSubnet2CIDR: The IP range (CIDR notation) for the private subnet in the second Availability Zone. Default: 10.8.21.0/24.
## Resources Created
- VPC: A new VPC with the specified CIDR block.
- Subnets: Public and private subnets in two Availability Zones.
- Internet Gateway: An Internet Gateway attached to the VPC.
- Route Tables: Route tables for public and private subnets.
- Security Group: A security group with no ingress rules.
## Outputs
- VPC: The ID of the created VPC.
- PublicSubnets: A list of the public subnets.
- PrivateSubnets: A list of the private subnets.
- PublicSubnet1: The ID of the public subnet in the first Availability Zone.
- PublicSubnet2: The ID of the public subnet in the second Availability Zone.
- PrivateSubnet1: The ID of the private subnet in the first Availability Zone.
- PrivateSubnet2: The ID of the private subnet in the second Availability Zone.
- NoIngressSecurityGroup: The ID of the security group with no ingress rules.
## Screenshots

![App Screenshot](https://snipboard.io/LtFIDN.jpg)
![App Screenshot](https://snipboard.io/RCe5si.jpg)
![App Screenshot](https://snipboard.io/nkoitg.jpg)
![App Screenshot](https://snipboard.io/oQ1vlm.jpg)



## 🔗 Links

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](http://linkedin.com/in/samuel-tettey-fio/)



## Authors

- [@bigsam233](https://github.com/bigsam233) on GitHub

