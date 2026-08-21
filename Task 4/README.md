# Task 4 — Immutable E-commerce Deployment with ECS & ECR

## Project Overview

Containerize and deploy the Evershop application using Amazon ECS on EC2 instances with Amazon ECR for container image storage. Application configuration is managed through AWS Systems Manager Parameter Store, with AWS CodePipeline and CodeBuild planned for automated CI/CD and zero-downtime blue/green deployments.

## Architecture

The following diagram represents the AWS infrastructure designed for the containerized Evershop application deployment.

![Task 4 ECS and ECR Architecture](architecture/task-4-ecs-ecr-architecture.jpeg)

## Amazon ECR Private Repository

Created a private Amazon ECR repository named `evershop` for storing Evershop container images.

![ECR Private Repository](screenshots/15-ecr-private-repository.png)

## AWS Systems Manager Parameter Store

Created Standard String parameters in AWS Systems Manager Parameter Store for Evershop application configuration.

![SSM Parameter Store](screenshots/16-ssm-parameter-store.png)

The configured parameters are:

- `/evershop/app/environment` — `production`
- `/evershop/app/port` — `3000`
