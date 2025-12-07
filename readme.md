## 1. CloudFormation

- This assignment includes:

- Creating AWS resources using Infrastructure as Code (IaC)

- Writing YAML/JSON CloudFormation templates

- Deploying stacks for EC2, VPC, S3, IAM roles, Security Groups

- Updating and deleting stacks

- Understanding stack lifecycle events

### Skills Gained: IaC, automation, repeatable deployments

## 2. Database Assignment (RDS)

- This folder contains tasks related to:

- Creating Amazon RDS instances

- Configuring MySQL/PostgreSQL engines

- Setting security groups & parameter groups

- Connecting RDS to an EC2 instance

- Understanding backups, Multi-AZ, and snapshots

- Skills Gained: Managed databases, networking, security

## 3. S3 Assignment

### Focused on:

- Creating S3 buckets

- Enabling versioning

- Object lifecycle policies

- Bucket policies & access control

- Static website hosting on S3

- Skills Gained: Object storage, website hosting, bucket security

## 4. IAM and CloudWatch Assignment

### Includes:

- Creating IAM users, groups, and roles

- Applying IAM policies (JSON)

- Enabling MFA

- CloudWatch metrics & log groups

- Creating alarms for EC2 CPU monitoring

- Skills Gained: Security, monitoring, identity management

## 5. VPC Assignment

### This involves:

- Creating custom VPC

- Public & private subnets

- Internet Gateway (IGW)

- NAT Gateway

- Route tables

- Launching EC2 inside custom VPC

- Skills Gained: Networking, VPC security, routing

## 6. EC2 + EFS Assignment

### Tasks include:

- Launching EC2

- Creating EFS filesystem

- Mounting EFS into EC2 using NFS

- Understanding shared storage across instances

- Skills Gained: Scalable storage, EC2 configuration

## 7. ELB & Auto Scaling Group Assignment

### Includes:

- Creating Application Load Balancers (ALB)

- Target groups and health checks

- Creating Auto Scaling Groups (ASG)

- Scaling policies & CloudWatch integration

- Skills Gained: High availability, elasticity

## 8. Lambda & Elastic Beanstalk Assignment

- Writing AWS Lambda functions

- Managing triggers (S3, SNS, API Gateway)

- Deploying applications on Elastic Beanstalk

- Understanding environments & scaling

- Skills Gained: Serverless, Platform as a Service (PaaS)

## 9. Project-1 A multi tier website using AWS EC2

### This project demonstrates the design and deployment of a multi-tier architecture using core AWS services such as EC2, RDS, and Security Groups.It showcases how a web server and a database server operate in separate tiers while communicating securely to deliver a dynamic application.

### Architecture Overview

- The project implements a 2-tier architecture:

### Tier 1 – Web/Application Layer (EC2)

- Launched an EC2 instance running Ubuntu.

- Configured a Security Group allowing incoming traffic (HTTP/HTTPS/SSH).

- Installed:
- Apache2 (Web server)
- PHP (Backend logic)
- MySQL client (To connect to RDS)
- Replaced the default Apache HTML page with a custom PHP form containing:
- Name field
- Email field
- Submit button

### Tier 2 – Database Layer (Amazon RDS)

- Created an Amazon RDS MySQL instance.

- Configured a separate Security Group allowing traffic only from the EC2 instance.

- Received the RDS Endpoint and used it in the PHP code to connect from EC2.

- Created a MySQL table with fields:
- name
- email
- Verified that form submissions insert data correctly into the RDS table.

## End-to-End Workflow

- User opens the EC2 public IP in the browser.

- The custom HTML/PHP form appears.

- User enters name and email → clicks Submit.

- PHP code connects to the RDS MySQL database using:
- Hostname (RDS endpoint)
- Username
- Password

- The data is successfully inserted into the MySQL table.

- Verified insertion by logging into MySQL from EC2 using:

- `mysql -h <RDS-ENDPOINT> -u <username> -p`

### Key AWS Concepts Demonstrated

- EC2 provisioning & Apache web server setup
- Security Group design for multi-tier architectures
- Installation and integration of Apache + PHP + MySQL
- RDS MySQL instance creation and VPC inter-resource connectivity
- Dynamic form handling & backend DB connectivity
- Storing and retrieving data from MySQL in the cloud

### Outcome

- A fully functional multi-tier dynamic website running on AWS where users submit data through a front-end application hosted on EC2, and the data is securely stored in an Amazon RDS MySQL database.

## 9. Project-2 – Publishing SNS Messages Privately

- Creating SNS topics

- Publishing messages through CLI / console

- IAM permissions for SNS publish

- Private SNS notifications

- Skills Gained: Notification services, secure messaging
