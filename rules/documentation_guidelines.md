# Documentation Guidelines

## General
- All code, APIs, and user-facing features must be thoroughly documented.
- Follow Windsurf Master Global Rules and workspace-specific documentation standards.

## Code Documentation
- All exported functions, classes, and components must have JSDoc or TSDoc comments.
- All modules must include a README with usage, configuration, and examples.
- All architectural decisions must be documented in ADRs and linked in `decisionLog.md`.
- All code must include type annotations and interface definitions.

## API Documentation
- All public APIs must be documented in OpenAPI (Swagger) format.
- Each endpoint must have request/response schemas, authentication, and error codes.
- All API changes must be reflected in the documentation before deployment.

## User Documentation
- All user-facing features must have guides in `/docs`.
- All onboarding and setup flows must be documented with screenshots and step-by-step instructions.
- All error messages must be actionable and link to relevant docs.

## Review
- Documentation must be reviewed as part of every PR.
- No feature is complete until documentation is updated.
