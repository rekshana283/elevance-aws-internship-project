# Task 2 — Secure RDS Deployment with IAM & Rotation

## Project Overview

Deploy a secure Multi-AZ MySQL Amazon RDS database for the Evershop application in private subnets with no public access. The architecture includes IAM database authentication, TLS-only connections, AWS Secrets Manager credential management with automatic rotation, encryption, backups, and point-in-time recovery.

## Architecture

The following diagram represents the AWS infrastructure designed for the secure Evershop RDS deployment.

![Task 2 Architecture](architecture/architecture-diagram.jpeg)

## RDS DB Subnet Group

Created the Evershop RDS DB subnet group using private database subnets across two Availability Zones.

![RDS Subnet Group](screenshots/13-rds-subnet-group.png)

## RDS Free Plan Limitation

Verified that the AWS Free Plan currently provides only Single-AZ deployment for the MySQL RDS configuration, while the project requirement specifies Multi-AZ deployment. The RDS database was therefore not created.

![RDS Free Plan Limitation](screenshots/14-rds-multiaz-free-plan-limitation.png)
