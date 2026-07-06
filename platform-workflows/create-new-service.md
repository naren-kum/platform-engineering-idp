# Create New Service Workflow

## Purpose

This workflow defines how a development team can request and create a new service using the platform golden path.

The goal is to reduce manual setup, improve consistency and make sure every new service starts with the required platform standards.

## Workflow Steps

1. Developer requests a new service
2. Platform team reviews the service type and requirements
3. Correct golden path template is selected
4. Repository structure is created
5. Dockerfile and CI/CD template are added
6. Required environment variables are documented
7. Secrets are identified and linked to approved secret stores
8. Health endpoint requirement is confirmed
9. Initial non-production deployment is prepared
10. Monitoring and operational readiness checks are added

## Required Inputs

| Input | Description |
|---|---|
| Service name | Name of the new service |
| Owner team | Team responsible for the service |
| Runtime | Runtime or framework used by the service |
| Application port | Port exposed by the application |
| Health endpoint | Endpoint used for health checks |
| Deployment target | Kubernetes or ECS |
| Database requirement | Whether the service needs a database |
| Secrets required | Runtime secrets needed by the service |

## Expected Output

The workflow should produce:

- Service repository structure
- Dockerfile
- CI/CD pipeline definition
- Environment configuration
- Secret requirements
- Health check configuration
- Initial deployment path
- Service onboarding record

## Platform Guardrails

- Use approved base images
- Do not store secrets in source control
- Use non-root containers where possible
- Include health checks
- Follow standard image tagging
- Use approved CI/CD pipeline templates
- Ensure logs are written to stdout/stderr