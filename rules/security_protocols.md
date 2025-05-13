# Security Protocols

## General
- Follow all security requirements in Windsurf Master Global Rules and workspace overrides.
- All API keys and secrets are stored using Keytar or OS keychain, never in plaintext or source code.
- Never log or expose API keys, tokens, or sensitive user data in any logs, UI, or error messages.
- All configuration and secrets must be loaded from environment variables or secure storage only.

## Electron
- Enable contextIsolation and sandboxing in all BrowserWindows.
- Never expose Node.js or Electron APIs directly to the renderer process.
- Validate and sanitize all IPC messages; use strict input/output schemas.
- Use Electron's secure defaults for window creation (no nodeIntegration, no remote module, etc.).
- All file operations must be validated and checked for path traversal and injection attacks.

## React
- Sanitize all user input and output with trusted libraries.
- Escape all dynamic HTML; never use dangerouslySetInnerHTML except with explicit review.
- Use HTTPS for all external API calls.

## Node.js
- Use helmet, cors, and other security middleware for any local API servers.
- Validate all incoming data and API responses.
- Never use deprecated or unsafe Node.js APIs.

## LLM/Media APIs
- All API requests must be authenticated and rate-limited.
- Validate all responses and handle errors securely.
- Never send user PII or sensitive data to third-party APIs unless explicitly required and documented.

## Git
- Never commit secrets, API keys, or credentials to the repository.
- Use .gitignore and pre-commit hooks to prevent accidental leaks.

## Compliance
- Follow OWASP Top 10 for Electron, Node.js, and React.
- Regularly audit dependencies for vulnerabilities.
- All security incidents must be logged and reported per incident response workflow.
