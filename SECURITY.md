# Security Policy

## Reporting a vulnerability

If you discover a security vulnerability in any GlycemicGPT repository, **please do not open a public issue.** Instead:

1. **Email:** Send details to the maintainer via [GitHub private vulnerability reporting](https://github.com/GlycemicGPT/GlycemicGPT/security/advisories/new)
2. **Include:** A description of the vulnerability, steps to reproduce, and any potential impact
3. **Response time:** We aim to acknowledge reports within 48 hours and provide a fix timeline within 7 days

## Scope

This policy covers all repositories under the [GlycemicGPT](https://github.com/GlycemicGPT) organization.

## Automated scanning

All repositories use automated security scanning:
- **SAST:** Semgrep (Python, TypeScript, Kotlin)
- **DAST:** ZAP active scanning, Nuclei templates
- **Dependencies:** OSV-Scanner, Renovate vulnerability alerts
- **Secrets:** GitGuardian

Findings are tracked as GitHub Issues and resolved in the normal development workflow. See [docs/security-testing.md](https://github.com/GlycemicGPT/GlycemicGPT/blob/develop/docs/security-testing.md) for details.

## Supported versions

Only the latest release on the `main` branch is supported with security fixes. Development builds on `develop` receive fixes as part of normal development.
