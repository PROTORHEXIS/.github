# Contributing to PROTORHEXIS

[简体中文](../../CONTRIBUTING.md) · **English** · [Français](CONTRIBUTING.fr.md) · [Español](CONTRIBUTING.es.md) · [Русский](CONTRIBUTING.ru.md)

We welcome issue reports, research leads, design discussions, documentation improvements and code contributions where each repository permits them. This is a **default collaboration guide**; it does not promise that every repository accepts external contributions.

## 1. Confirm scope and permissions

1. Read the target repository's `README.md`, `CONTRIBUTING.md`, `AGENTS.md`, security policy and task-specific instructions where present.
2. Confirm whether it accepts Issues, Pull Requests and outside contributions. Never disclose the contents, configuration or access rights of a private repository merely because you are working with the organization.
3. Repository-specific instructions, approved specifications and ADRs, maintainer decisions, branch protections and existing review gates take precedence over this general guide. Explain conflicts and ask maintainers to decide rather than lowering higher-authority requirements.
4. Search existing issues and PRs first. Propose significant changes to architecture, interfaces, governance, data handling or public commitments before implementation.

## 2. Submit reviewable, evidence-backed changes

- In Issues, describe observed behavior, expected behavior, reproduction conditions, impact and available evidence. Label assumptions as assumptions.
- Keep PRs focused. Describe their purpose, affected contracts or repositories, actual tests and validation, compatibility, risks and rollback or mitigation.
- Distinguish design targets, implemented facts and remaining gaps. A check that was not run is `NOT RUN` or `UNVERIFIED`, never `PASS`.
- Tie any passing verification claim to the execution environment, commands, results and exact source commit. Local checks are not equivalent to remote CI, deployment readiness or release approval.
- Avoid unrelated rewrites and deletions. Data migrations, permission changes, destructive operations, sensitive disclosures and cross-project contract changes require the applicable explicit authorization.
- Never upload secrets, personal data, private logs, unapproved research materials or excerpts from private code. For vulnerabilities, use the [security policy](SECURITY.en.md).

## 3. Review and status

Use statuses such as `PROPOSED`, `IMPLEMENTED`, `STATIC_VERIFIED`, `LOCAL_PASS`, `REMOTE_CI_PASS`, `UNVERIFIED`, `BLOCKED` and `HOLD` according to actual evidence. These are different states, not interchangeable labels.

Submitting a PR is not approval. The target repository's reviewers decide according to its review rules, required checks, exact HEAD and release gates. Existing HOLD or freeze decisions are not automatically lifted by this guide or an ordinary PR.

## 4. Collaboration conduct

Respect people and rigorously examine ideas. Evidence-backed disagreement and constructive correction are welcome; harassment, discrimination, exposure of private information and personal attacks are not. Raise conduct concerns through an appropriate maintainer channel without publicly spreading sensitive details.
