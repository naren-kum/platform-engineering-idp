# Golden Paths

## What is a Golden Path?

A golden path is an approved and reusable way for developers to build, deploy and operate a service.

It provides a clear route from source code to production while including the standards required by platform, security and operations teams.

## Golden Path Workflow

1. Create service repository
2. Add Dockerfile
3. Add CI/CD pipeline
4. Add infrastructure configuration
5. Configure environment variables and secrets
6. Add health endpoint
7. Deploy to non-production
8. Validate logs, metrics and health checks
9. Promote to production
10. Monitor and support service

## Service Requirements

Every onboarded service should include:

- README
- Dockerfile
- CI/CD pipeline
- Health endpoint
- Environment variable documentation
- Secrets documentation
- Deployment configuration
- Monitoring and alerting requirements
- Runbook

## Developer Outcome

Developers should be able to onboard a new service without manually designing the full deployment process from scratch.

The platform should provide reusable patterns for:

- Build
- Test
- Scan
- Package
- Deploy
- Monitor
- Support