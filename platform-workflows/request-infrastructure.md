# Request Infrastructure Workflow

## Purpose

This workflow defines how teams request cloud infrastructure through the platform.

The goal is to standardise infrastructure requests and ensure cloud resources are provisioned securely, consistently and with proper ownership.

## Workflow Steps

1. Developer or team submits infrastructure request
2. Platform team reviews the requirement
3. Required AWS resources are identified
4. Terraform module or reusable pattern is selected
5. Environment-specific variables are prepared
6. Security and access requirements are reviewed
7. Cost and ownership tags are confirmed
8. Terraform plan is generated
9. Approval is completed
10. Infrastructure is provisioned
11. Outputs are shared with the requesting team

## Required Inputs

| Input | Description |
|---|---|
| Requesting team | Team requesting infrastructure |
| Environment | Dev, QA, staging or production |
| Resource type | Example: S3, RDS, ECS service, IAM role |
| Business purpose | Why the resource is needed |
| Network requirements | VPC, subnet and access requirements |
| Access requirements | IAM roles, users or services requiring access |
| Data sensitivity | Whether sensitive data is involved |
| Backup requirement | Whether backup or retention is required |
| Estimated usage | Expected workload or traffic |
| Owner | Person or team responsible for the resource |

## Platform Standards

Infrastructure should follow these standards:

- Provision using Terraform
- Use approved modules where possible
- Store state remotely
- Apply standard naming conventions
- Apply required tags
- Follow least privilege access
- Avoid public exposure unless approved
- Enable monitoring where required
- Document outputs and dependencies

## Approval Considerations

Production infrastructure may require additional review for:

- Security
- Cost
- Network exposure
- Data protection
- Backup and restore
- High availability
- Operational support