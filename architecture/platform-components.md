# Platform Components

This document defines the main components of the Internal Developer Platform and their responsibilities.

## Component Overview

| Component | Responsibility |
|---|---|
| Source Control | Stores application and platform code |
| CI/CD | Builds, tests, scans and deploys services |
| Infrastructure as Code | Provisions and manages cloud resources |
| Container Registry | Stores versioned container images |
| Deployment Platform | Runs application workloads |
| Secrets Management | Provides secure runtime secrets |
| Observability | Provides logs, metrics, dashboards and alerts |
| Runbooks | Supports operations and incident response |

## Source Control

GitHub is used for source control, pull requests and code review workflows.

Platform standards should define:

- Repository structure
- Branching strategy
- Pull request rules
- Code owners
- Release tagging
- Commit message expectations

## CI/CD

Jenkins and GitHub Actions are used for CI/CD automation.

Pipelines should standardise:

- Build
- Test
- Security scanning
- Docker image creation
- Image tagging
- Registry push
- Deployment
- Rollback

## Infrastructure as Code

Terraform is used to provision cloud infrastructure.

IaC standards should include:

- Remote state
- Environment-specific variables
- Reusable modules
- Naming conventions
- Tagging standards
- Pull request review
- Plan and approval workflow

## Container Platform

Docker is used for application packaging.

Kubernetes or ECS can be used as the container orchestration platform depending on the workload and organisation requirements.

Container standards should include:

- Approved base images
- Multi-stage builds where appropriate
- Non-root users
- Health checks
- Runtime configuration through environment variables
- Secrets from approved secret stores

## Observability

Observability should provide visibility into service health and behaviour.

The platform should support:

- Logs
- Metrics
- Dashboards
- Alerts
- Health checks
- Incident investigation
- Post-incident review

## Security

Security should be built into the platform workflow.

The platform should support:

- IAM least privilege
- Secrets management
- Container image scanning
- Dependency scanning
- TLS standards
- Access reviews
- Audit visibility