# agents.md — security-advisories

## Repository Overview

Central registry for published security advisories across the ownCloud project. This repository provides a structured, public record of disclosed and resolved security vulnerabilities.

- **Classification:** Community / Meta
- **Activity Status:** Maintenance
- **License:** No license detected
- **Language:** None (advisory records only)

## Architecture & Key Paths

- `README.md` — Repository description

This is a minimal repository. Advisory content is managed through GitHub Security Advisories.

## Development Conventions

- Advisories follow responsible disclosure timelines
- No code or build processes in this repository

## Build & Test Commands

No build or test commands. This is a documentation-only repository.

## Important Constraints

- **No license file detected:** The OSPO is working on formalizing license status.
- Do not introduce new **copyleft-licensed dependencies** (GPL, AGPL, LGPL, MPL) without explicit discussion in an issue first. This is especially important for repos that are migrating to or already under Apache 2.0, as copyleft dependencies would block or complicate that migration.
- **Copyleft + Apache 2.0 migration:** Not directly applicable to this meta repository, but the OSPO license migration strategy applies to all ownCloud repositories.
- **Responsible disclosure:** Security vulnerabilities must follow responsible disclosure practices and should not be reported as public issues.


## OSPO Policy Constraints

### GitHub Actions
- **Only** use actions owned by `owncloud`, created by GitHub (`actions/*`), verified on the GitHub Marketplace, or verified by the ownCloud Maintainers.
- Pin all actions to their full commit SHA (not tags): `uses: actions/checkout@<SHA> # vX.Y.Z`
- Never introduce actions from unverified third parties.

### Dependency Management
- Dependabot is configured for automated dependency updates.
- Review and merge Dependabot PRs as part of regular maintenance.
- Do not introduce new dependencies without discussion in an issue first.

### Git Workflow
- **Rebase policy**: Always rebase; never create merge commits. Use `git pull --rebase` and `git rebase` before pushing.
- **Signed commits**: All commits **must** be PGP/GPG signed (`git commit -S -s`).
- **DCO sign-off**: Every commit needs a `Signed-off-by` line (`git commit -s`).
- **Conventional Commits & Squash Merge**: Use the [Conventional Commits](https://www.conventionalcommits.org/) format where the repository enforces it. Many repos use squash merge, where the PR title becomes the commit message on the default branch — apply Conventional Commits format to PR titles as well. A reusable GitHub Actions workflow enforces this.

## Context for AI Agents

- This repository has no code, build system or CI.
- It serves as a public record of resolved security vulnerabilities.
- For reporting new vulnerabilities, use the ownCloud Security Policy at https://github.com/owncloud/.github/blob/main/SECURITY.md.
