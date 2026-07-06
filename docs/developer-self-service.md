# Developer Self-Service

## Overview

Developer self-service allows engineering teams to create, deploy and operate services using approved platform workflows without waiting for repeated manual DevOps tasks.

The goal is not to remove platform control. The goal is to provide safe, reusable and standardised workflows that developers can follow independently.

## Self-Service Workflows

The platform should support the following workflows:

* Create a new service
* Request infrastructure
* Deploy to an environment
* Configure environment variables
* Request secrets
* View logs and dashboards
* Access runbooks
* Understand production readiness requirements

## Example Workflow: Create New Service

1. Developer selects a service template
2. Repository is created with standard structure
3. Dockerfile and CI/CD pipeline are included
4. Required platform files are generated
5. Service owner completes onboarding information
6. Pull request is reviewed
7. Service is deployed to non-production
8. Monitoring and health checks are validated

## Benefits

* Reduces manual DevOps effort
* Improves consistency between teams
* Speeds up service onboarding
* Reduces deployment mistakes
* Makes operational requirements visible early
* Helps teams follow approved platform standards

## Guardrails

Self-service should include guardrails such as:

* Approved templates
* Required code review
* CI/CD validation
* Secrets management
* Infrastructure approval where needed
* Security scanning
* Production readiness checks
