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

## AWS WAF Protection Pack

Created the AWS WAF protection pack named `EverShop Cloud Front WAF` to protect the Evershop CloudFront distribution against common web application threats.

![WAF Protection Pack](screenshots/10-waf-protection-pack.png)

## WAF Resources and Protection Packs

Configured the WAF protection resources and Web ACL for the Evershop CloudFront distribution.

![WAF Resources and Protection Packs](screenshots/11-waf-resources-and-protection-packs.png)

## CloudFront Web Application Firewall

Enabled AWS WAF security protection for the Evershop CloudFront distribution to help protect the application from common web threats and vulnerabilities.

![CloudFront WAF Security](screenshots/12-cloudfront-waf-security.png)
