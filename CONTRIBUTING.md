# Contributing to GlycemicGPT

Thank you for your interest in contributing to GlycemicGPT. This guide covers the org-wide conventions that apply to all repositories. For repo-specific setup instructions, see the CONTRIBUTING.md in the relevant repository.

## Safety First

GlycemicGPT processes real diabetes management data. **Every repository in this organization must treat medical safety as a first-class concern.** This means:

- AI outputs must be labeled as suggestions, never medical advice
- Insulin dosing suggestions must include disclaimers and verification prompts
- Wrong glucose numbers and incorrect insulin calculations are safety issues, not just bugs
- Safety limits are enforced at the platform level and must not be bypassed by plugins or UI changes
- Device control features (if any) are never shipped in pre-built releases

If you're unsure whether a change has safety implications, ask in the PR -- a maintainer will review.

## Repository-Specific Guides

Each repo has its own CONTRIBUTING.md with setup instructions, testing requirements, and development workflows:

| Repository | Contributing Guide |
|-----------|-------------------|
| [GlycemicGPT](https://github.com/GlycemicGPT/GlycemicGPT) (main platform) | [CONTRIBUTING.md](https://github.com/GlycemicGPT/GlycemicGPT/blob/develop/CONTRIBUTING.md) |

*Additional repos will be listed here as they're created.*

## Org-Wide Conventions

These apply to all repositories in the GlycemicGPT organization:

### Branching & PRs
- All PRs target `develop`, never `main` directly
- `develop` is the integration branch; `main` is the stable release
- Promotion from `develop` to `main` is a maintainer-only action via promotion PR

### Commits
- Use [Conventional Commits](https://www.conventionalcommits.org/): `feat:`, `fix:`, `docs:`, `chore:`, `refactor:`, `test:`
- Keep commit messages concise (under 72 characters for the subject line)
- No AI attribution in commits or code -- all commits are authored solely by the human developer

### Code Review
- All PRs require at least one approving review from a code owner
- CI must pass before merge
- Security scan findings must be addressed, not ignored

### Security
- Never commit secrets, API keys, tokens, or credentials
- Security vulnerabilities should be reported privately -- see [SECURITY.md](SECURITY.md)
- Suppressed security findings must include a documented reason

## Governance

Project roles (Contributor, Committer, Maintainer) and the decision-making process are documented in [GOVERNANCE.md](https://github.com/GlycemicGPT/GlycemicGPT/blob/develop/GOVERNANCE.md).

## Code of Conduct

All contributors are expected to follow our [Code of Conduct](CODE_OF_CONDUCT.md).
