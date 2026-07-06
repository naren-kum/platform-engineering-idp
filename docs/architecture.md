# IDP Architecture

## Overview

The Internal Developer Platform provides reusable standards and workflows that help engineering teams build, deploy and operate services consistently.

The platform is designed around a golden path model where developers can follow approved patterns for service creation, CI/CD, infrastructure provisioning, deployment and operational readiness.

## High-Level Flow

Developer submits or updates application code in GitHub.

The CI/CD pipeline then validates the change, runs tests, builds a Docker image, performs security checks and pushes the image to a registry.

The deployment platform then deploys the application to Kubernetes or ECS using environment-specific configuration and runtime secrets.

Observability tooling provides logs, metrics, dashboards and alerts for operational support.

## Platform Flow

1. Developer creates or updates a service repository
2. Pull request is reviewed and approved
3. CI/CD pipeline runs build, test and scan stages
4. Docker image is created and pushed to the image registry
5. Infrastructure or deployment configuration is applied
6. Service is deployed to Kubernetes or ECS
7. Runtime configuration and secrets are injected securely
8. Health checks confirm service availability
9. Logs, metrics and alerts support ongoing operations

## Key Components

| Component                             | Purpose                                  |
| ------------------------------------- | ---------------------------------------- |
| GitHub                                | Source control and pull request workflow |
| Jenkins / GitHub Actions              | CI/CD automation                         |
| Terraform                             | Infrastructure provisioning              |
| Docker                                | Application packaging                    |
| Kubernetes / ECS                      | Container orchestration                  |
| AWS                                   | Cloud platform                           |
| CloudWatch / Prometheus / Grafana     | Monitoring and observability             |
| Secrets Manager / SSM Parameter Store | Runtime secrets and configuration        |

## Design Principles

* Standardise common delivery workflows
* Reduce manual deployment effort
* Improve environment consistency
* Provide reusable templates
* Keep secrets outside source code
* Build observability into every service
* Support production readiness from the start
* Make developer onboarding easier
* Improve reliability through repeatable patterns
