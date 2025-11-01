# Security Policy

## Supported Versions

We release patches for security vulnerabilities in the following versions:

| Version | Supported          |
| ------- | ------------------ |
| main    | :white_check_mark: |
| contract-guardian | :white_check_mark: |
| < 1.0   | :x:                |

## Reporting a Vulnerability

We take the security of Cerno Docs seriously. If you discover a security vulnerability, please follow these steps:

### 🔒 Private Disclosure

**DO NOT** open a public issue for security vulnerabilities.

Instead, please report security issues by:

1. **Email**: Send details to the repository owner (check GitHub profile)
2. **GitHub Security**: Use GitHub's private vulnerability reporting feature

### 📋 What to Include

Please provide:
- Type of vulnerability
- Full path to the source file(s) related to the vulnerability
- Location of the affected code (tag/branch/commit/direct URL)
- Step-by-step instructions to reproduce the issue
- Proof-of-concept or exploit code (if available)
- Impact of the vulnerability
- Suggested fix (if you have one)

### ⏱️ Response Timeline

- **Initial Response**: Within 48 hours
- **Status Update**: Within 7 days
- **Fix Timeline**: Varies by severity
  - Critical: Within 7 days
  - High: Within 30 days
  - Medium: Within 90 days
  - Low: Next release

### 🏆 Recognition

We appreciate responsible disclosure. If you'd like:
- We can credit you in the release notes (with your permission)
- We'll acknowledge your contribution in SECURITY.md

## Security Best Practices for Users

### API Keys
- **Never commit** `.env` files with real API keys
- Use environment variables or secret management services
- Rotate keys regularly
- Use separate keys for development and production

### Deployment
- **Always use HTTPS** in production
- Keep dependencies updated: `pip install -r requirements.txt --upgrade`
- Use firewall rules to restrict access
- Monitor logs for suspicious activity

### Docker
- Don't run containers as root (use non-root user)
- Scan images for vulnerabilities: `docker scan cerno-docs`
- Use specific image versions, not `latest`
- Keep Docker and base images updated

### Data Privacy
- This system processes documents locally by default
- Be aware that LLM API calls send data to external services (Google Gemini)
- For sensitive documents, consider:
  - Self-hosted LLM alternatives
  - On-premises deployment
  - Data anonymization before processing

## Known Security Considerations

### LLM API Usage
- User queries and document chunks are sent to Google Gemini API
- Responses may be logged by the LLM provider
- Consider data residency and compliance requirements

### File Upload
- File size limits enforced (configurable)
- File type validation implemented
- Malicious file scanning recommended for production

### Dependencies
- Regular updates recommended
- Run `pip audit` to check for known vulnerabilities
- Monitor GitHub Security Advisories

## Security Updates

Security patches will be:
- Released as soon as possible after confirmation
- Documented in release notes
- Announced in repository README
- Tagged with `security` label

## Questions?

For general security questions (not vulnerabilities), please open a regular GitHub issue with the `question` label.

---

**Thank you for helping keep Cerno Docs secure!** 🔐
