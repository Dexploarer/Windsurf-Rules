# API Standards

## General
- All APIs must follow RESTful or RPC conventions as appropriate.
- Use consistent naming, versioning, and error handling across all APIs.
- All public APIs must be documented in OpenAPI (Swagger) format.
- All endpoints must have input/output schemas and validation.

## Versioning
- All APIs must be versioned (e.g., /v1/, /v2/).
- Breaking changes require a new major version.
- Deprecations must be documented and communicated in advance.

## Documentation
- All endpoints must have request/response examples, authentication requirements, and error codes.
- API docs must be updated before each release.

## Security
- All endpoints must require authentication (API key, OAuth, etc.).
- Validate and sanitize all inputs and outputs.
- Never expose internal errors, stack traces, or sensitive data in responses.
- Implement rate limiting and abuse prevention.

## Error Handling
- Use standard HTTP status codes and error objects.
- All errors must have clear, actionable messages for clients.
- Log all errors securely for auditing.

## Testing
- All APIs must have automated tests for all endpoints, including error and edge cases.
- Test coverage must be >90% for all API code.

## Review
- All API changes must be reviewed and approved before deployment.
