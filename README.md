# Secure Internal Application Migration to AWS

## Project Overview

This project simulates the migration of a legacy internal business application from on-premises infrastructure to AWS.

The organisation currently operates the application on aging hardware with limited monitoring, manual infrastructure management, and traditional administrative access.

The objective is to design and deploy a secure, repeatable AWS environment that improves security, visibility, and infrastructure management while reducing direct exposure of the application server.

## Business Requirements

The proposed AWS environment must:

- Host the internal application securely within AWS.
- Prevent direct public access to the application server.
- Provide secure administrative access without exposing SSH to the internet.
- Apply least-privilege access controls.
- Encrypt sensitive infrastructure where appropriate.
- Provide monitoring and logging.
- Record administrative AWS activity for auditing.
- Allow the infrastructure to be reproduced using Infrastructure as Code.

## Proposed AWS Services

- Amazon VPC
- Amazon EC2
- AWS IAM
- AWS Systems Manager Session Manager
- Amazon CloudWatch
- AWS CloudTrail
- Amazon EBS
- AWS KMS
- VPC Flow Logs
- Terraform

## Infrastructure as Code

Terraform will be used to provision and manage the AWS infrastructure. This allows the environment to be version controlled, reviewed, reproduced, and modified consistently.