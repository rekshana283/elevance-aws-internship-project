# Task 1 – AWS Web Application Infrastructure

## Project Overview

This task focuses on building the core AWS infrastructure for the Evershop web application.

The infrastructure was configured using Amazon VPC, subnets, route tables, security groups, Amazon EC2, an Application Load Balancer, a target group, and Amazon CloudFront.

---

## Architecture

The following diagram represents the AWS infrastructure created for the Evershop application.

![Evershop Architecture](architecture/evershop-architecture.jpeg)

---

## 1. VPC

Created the Evershop VPC with an IPv4 CIDR block of `10.0.0.0/16`.

![VPC Configuration](screenshots/01-vpc.png)

---

## 2. Subnets

Configured public and private subnets across multiple Availability Zones within the Evershop VPC.

![Subnet Configuration](screenshots/02-subnets.png)

---

## 3. Internet Gateway

Configured an Internet Gateway to provide internet connectivity for the public network.

![Internet Gateway](screenshots/03-internet-gateway.png)

---

## 4. Route Tables

Configured route tables to control traffic between the public and private subnets and the required network destinations.

![Route Tables](screenshots/04-route-tables.png)

---

## 5. Security Groups

Configured security groups for the Application Load Balancer and web tier to control inbound and outbound traffic.

![Security Groups](screenshots/05-security-groups.png)

---

## 6. EC2 Instance

Launched an Amazon EC2 instance to host the web application.

![EC2 Instance](screenshots/06-ec2-instance.png)

---

## 7. Target Group

Created a target group and registered the EC2 web server as a target for the Application Load Balancer.

![Target Group](screenshots/07-target-group.png)

---

## 8. Application Load Balancer

Created an internet-facing Application Load Balancer and configured it to forward HTTP traffic to the target group.

![Application Load Balancer](screenshots/08-application-load-balancer.png)

---

## 9. CloudFront

Created an Amazon CloudFront distribution using the Application Load Balancer as the origin.

![CloudFront Distribution](screenshots/09-cloudfront.png)

---

## Security Configuration

Security groups were configured to control access to the EC2 instance and Application Load Balancer.

SSH access was configured using a restricted source IP rather than allowing unrestricted access.

AWS WAF, Route 53, and ACM configuration remain pending because the current AWS Free plan does not allow domain registration through Route 53.

---

## Cost Considerations

AWS resources were created with cost awareness.

The AWS account currently has promotional credits available, but chargeable services were enabled only when required for the project.

NAT Gateway was not created because it is not required for the current Task 1 implementation and can generate hourly and data-processing charges.

---

## Current Status

The core AWS infrastructure for Task 1 has been created and configured.

Implemented components:

- Amazon VPC
- Public and private subnets
- Internet Gateway
- Route tables
- Security groups
- Amazon EC2
- Target group
- Application Load Balancer
- Amazon CloudFront

Pending components:

- Route 53 domain
- ACM public certificate
- AWS WAF
- HTTPS/HSTS configuration
- Failover routing

These remaining components depend on domain registration and the current AWS account plan.
