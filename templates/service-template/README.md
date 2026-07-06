# Service Template

This template provides a standard starting point for onboarding a new backend service onto the platform.

It includes a basic Dockerfile, local Docker Compose example and health endpoint expectation.

## Purpose

The goal of this template is to give development teams a consistent starting point when creating a new service.

The template supports the platform golden path by including:

- Standard project structure
- Dockerfile pattern
- Docker Compose local runtime example
- Health endpoint expectation
- Runtime environment variable examples
- Non-root container pattern

## Expected Service Requirements

A service created from this template should include:

- Application source code
- Dockerfile
- Health endpoint
- Runtime configuration documentation
- CI/CD pipeline
- Deployment configuration
- Monitoring and alerting requirements
- Runbook

## Required Runtime Variables

| Variable | Required | Description |
|---|---|---|
| APP_ENV | Yes | Runtime environment |
| PORT | Yes | Application port |
| DATABASE_URL | If required | Database connection string |

## Health Endpoint

Every service should expose a health endpoint.

Recommended path:

`/health`

The health endpoint should confirm that the application process is running and able to respond to requests.

## Local Development

This template includes a `compose.yaml` file that can be used as a starting point for running the service locally with Docker Compose.

## Production Notes

Before production use, confirm:

- The correct runtime base image is used
- Secrets are not stored in source control
- The container runs as non-root
- Logs are written to stdout/stderr
- Health checks are configured
- Required environment variables are documented