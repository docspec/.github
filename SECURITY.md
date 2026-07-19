# Security Policy

## Reporting a Vulnerability

If you find a security vulnerability in any DocSpec project, please report it privately. Don't open a public issue.

Send details to the project maintainers through [GitHub's private vulnerability reporting](https://github.com/docspec/docspec/security/advisories/new), or by emailing the maintainers directly if that channel isn't available. Include:

- A description of the vulnerability
- Steps to reproduce
- Potential impact
- Any suggested fixes (optional)

We'll acknowledge receipt within 48 hours and follow up within 7 days with next steps and an expected timeline for a fix.

## Security Best Practices

When running DocSpec in production:

- Keep dependencies updated — run `cargo update` regularly and watch for `cargo audit` advisories
- Validate and sanitize document inputs before processing; DocSpec streams what it receives
- Run conversion services in isolated environments
- Monitor for unusual resource consumption during document processing — a malformed document shouldn't be able to exhaust memory, but defense in depth matters
