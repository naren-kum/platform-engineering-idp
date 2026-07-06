# Golden Path: .NET API

## Purpose

This golden path defines the standard approach for building, containerising and deploying a .NET API service.

It provides a repeatable pattern for teams building backend services using .NET and deploying them through the platform.

## Standard Service Requirements

A .NET API should include:

- Solution and project files
- Dockerfile using multi-stage build
- Health endpoint
- Environment-specific configuration
- CI/CD pipeline
- Runtime secrets through approved secret store
- Logging to stdout/stderr
- Deployment configuration
- Runbook

## Dockerfile Pattern

The standard .NET API Dockerfile should use a multi-stage build.

Build stage:

- Use .NET SDK image
- Copy project files first
- Run dotnet restore
- Copy source code
- Run dotnet publish

Runtime stage:

- Use ASP.NET runtime image
- Copy published output only
- Set ASPNETCORE_ENVIRONMENT
- Set ASPNETCORE_URLS
- Expose application port
- Run as non-root where possible
- Start the application DLL

## Required Runtime Configuration

| Variable | Purpose |
|---|---|
| ASPNETCORE_ENVIRONMENT | Sets runtime environment |
| ASPNETCORE_URLS | Defines listening URL and port |
| ConnectionStrings__DefaultConnection | Database connection string if required |

## CI/CD Stages

The pipeline should include:

1. Checkout source code
2. Restore dependencies
3. Build solution
4. Run tests
5. Build Docker image
6. Scan image
7. Push image to registry
8. Deploy to environment
9. Validate health endpoint

## Operational Readiness

Before production release:

- Health endpoint is available
- Logs are visible in the monitoring platform
- Required secrets are configured
- Database connectivity is validated
- Rollback image tag is known
- Alerts are configured
- Runbook is available