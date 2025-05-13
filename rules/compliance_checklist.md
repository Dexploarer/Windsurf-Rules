# Compliance Checklist

## Security
- All API keys and secrets are stored securely (Keytar/OS keychain).
- No secrets or sensitive data in logs, source, or git history.
- All dependencies are audited for vulnerabilities before release.
- All IPC and API endpoints are validated and sanitized.

## Privacy
- No user data is shared with third parties without explicit consent.
- All user data is encrypted at rest and in transit.
- All privacy policies are documented and accessible.

## Accessibility
- All UI components meet WCAG 2.1 AA accessibility standards.
- Keyboard navigation and screen reader support for all features.
- Color contrast and dark mode compliance.

## Documentation
- All features, APIs, and workflows are documented in Markdown and ADRs.
- All onboarding and error flows are documented for users and developers.

## Testing
- All code and features have automated tests and CI/CD checks.
- Manual QA performed before each release.

## Release
- All releases have a changelog and are tagged in git.
- All compliance items are checked and signed off before release.
