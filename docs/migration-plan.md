# Migration Plan

## 1. Background

Northstar Services Ltd currently operates an internal business application on ageing on-premises infrastructure.

The existing environment relies on manually managed infrastructure with limited monitoring and auditing capabilities. Rebuilding the environment is also difficult because the infrastructure configuration is not defined as code.

The organisation has decided to migrate the workload to Amazon Web Services (AWS) to improve security, visibility, maintainability and infrastructure consistency.

## 2. Migration Objectives

The migration aims to:

- Move the internal application from ageing on-premises infrastructure to AWS.
- Reduce direct exposure of the application server.
- Implement secure administrative access.
- Introduce Infrastructure as Code using Terraform.
- Apply least-privilege access controls.
- Improve monitoring and operational visibility.
- Introduce centralised auditing of AWS activity.
- Encrypt relevant storage.
- Create a repeatable infrastructure deployment process.

## 3. Security Requirements

The target environment should:

- Run the application server without a public IP address.
- Avoid exposing SSH directly to the internet.
- Use AWS Systems Manager Session Manager for administrative access.
- Restrict network traffic using security groups.
- Use IAM roles rather than storing AWS credentials on the server.
- Encrypt EBS storage.
- Record AWS API activity using CloudTrail.
- Monitor infrastructure using CloudWatch.
- Capture relevant network traffic metadata using VPC Flow Logs.

## 4. Migration Approach

The project will simulate a rehost migration of the existing application into an AWS EC2-based environment.

Terraform will provision the required AWS infrastructure to ensure that the target environment is repeatable and version controlled.

The migration will be completed in stages:

1. Design the target AWS architecture.
2. Provision networking infrastructure.
3. Configure security controls.
4. Deploy the EC2 application server.
5. Configure secure administrative access.
6. Deploy the sample internal application.
7. Configure monitoring and auditing.
8. Validate security and connectivity.
9. Document the final environment and migration outcomes.

## 5. Success Criteria

The migration will be considered successful when:

- The application runs successfully on AWS.
- The EC2 application server has no public IP address.
- Administrative access is available through Systems Manager Session Manager.
- No inbound SSH access from the internet is required.
- Infrastructure can be recreated using Terraform.
- Application and infrastructure health can be monitored.
- AWS administrative activity is auditable.
- Storage is encrypted.
- Security controls are validated and documented.