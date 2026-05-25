# CSP-451 GitHub Actions Seed Repo

![CI](https://github.com/Akkoirii/csp451-actions-seed/actions/workflows/ci.yml/badge.svg?branch=main)
![CodeQL](https://github.com/Akkoirii/csp451-actions-seed/actions/workflows/codeql.yml/badge.svg?branch=main)

Seed repository for the GitHub Actions CI/CD CheckPoint in CSP-451 — Computer Systems Projects.

The pipeline lints, formats, tests with coverage thresholds, runs npm audit, and analyzes the source with GitHub CodeQL on every push and pull request. Dependabot keeps npm packages and GitHub Actions versions current.

## Local Setup

1. Install Node.js 20 LTS
2. Install dependencies

```bash
npm ci
```

3. Run checks

```bash
npm run format:check
npm run lint
npm test
npm run audit:check
```

4. Run application

```bash
npm start
```

Visit http://localhost:3000

## Features Implemented

### Root Endpoint

GET /

Returns:

```json
{
  "status": "ok",
  "message": "Hello from CSP-451"
}
```

### Health Endpoint

GET /health

Returns:

```json
{
  "status": "healthy",
  "uptime": 0
}
```

## Testing

Tests are implemented using Jest and Supertest.

Coverage thresholds enforced:

- Statements: 80%
- Functions: 80%
- Lines: 80%
- Branches: 70%

## Code Scanning

Security checks include:

- GitHub CodeQL
- Dependabot
- npm audit

## Branch Protection

Main branch is protected using:

- Required pull requests
- Required status checks
- Up-to-date branch requirement