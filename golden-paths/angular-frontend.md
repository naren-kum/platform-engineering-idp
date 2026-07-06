# Golden Path: Angular Frontend

## Purpose

This golden path defines the standard approach for building, packaging and deploying an Angular frontend application.

It provides a repeatable pattern for frontend teams delivering web applications through the platform.

## Standard Service Requirements

An Angular frontend should include:

- package.json and package-lock.json
- Build command
- Environment configuration approach
- Dockerfile if containerised
- Static hosting or Nginx runtime pattern
- CI/CD pipeline
- Health or availability check
- Deployment documentation

## Build Pattern

The standard build process should include:

1. Install dependencies using npm ci
2. Run linting if required
3. Run tests if required
4. Build production assets
5. Package static output
6. Deploy to hosting platform or container image

## Container Pattern

If containerised, the frontend should use a multi-stage Dockerfile.

Build stage:

- Use Node.js image
- Copy package files first
- Run npm ci
- Copy source code
- Run production build

Runtime stage:

- Use Nginx image
- Copy built static files
- Configure routing if required
- Expose HTTP port

## Required Runtime Configuration

Frontend applications may require environment-specific configuration such as:

| Configuration | Purpose |
|---|---|
| API base URL | Backend API endpoint |
| Auth endpoint | Authentication provider |
| Environment name | Dev, QA, staging or production |
| Feature flags | Optional feature configuration |

## CI/CD Stages

The pipeline should include:

1. Checkout source code
2. Install dependencies
3. Run tests
4. Build frontend assets
5. Build container image or package static files
6. Scan image or package
7. Deploy to target environment
8. Validate application URL

## Operational Readiness

Before production release:

- Application URL is accessible
- Backend API endpoint is correct
- Routing works after refresh
- Static assets load correctly
- Logs or access logs are available
- Rollback approach is defined