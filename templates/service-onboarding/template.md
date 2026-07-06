# Service Onboarding Template

This template defines the minimum information required to onboard a new service onto the platform.

## Service Information

| Field               | Value               |
| ------------------- | ------------------- |
| Service Name        |                     |
| Owner Team          |                     |
| Runtime / Framework |                     |
| Repository URL      |                     |
| Deployment Target   | Kubernetes / ECS    |
| Application Port    |                     |
| Health Endpoint     |                     |
| Criticality         | Low / Medium / High |

## Build Information

| Question                                  | Answer |
| ----------------------------------------- | ------ |
| What command installs dependencies?       |        |
| What command runs tests?                  |        |
| What command builds or publishes the app? |        |
| What Dockerfile should be used?           |        |
| Are there build-time arguments?           |        |

## Runtime Configuration

| Variable     | Required    | Description                |
| ------------ | ----------- | -------------------------- |
| APP_ENV      | Yes         | Runtime environment        |
| DATABASE_URL | If required | Database connection string |

## Secrets

| Secret | Source                                    | Description |
| ------ | ----------------------------------------- | ----------- |
|        | AWS Secrets Manager / SSM Parameter Store |             |

## Observability

| Requirement  | Details       |
| ------------ | ------------- |
| Logs         | stdout/stderr |
| Metrics      |               |
| Dashboards   |               |
| Alerts       |               |
| Health Check |               |

## Operational Readiness

Before production deployment, confirm:

* Service has a health endpoint
* Logs are visible
* Required alerts are configured
* Secrets are not stored in source control
* Deployment rollback approach is understood
* Runbook exists
* Service owner is documented
* Required environment variables are documented
