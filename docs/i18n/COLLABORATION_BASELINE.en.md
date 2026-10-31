# PROTORHEXIS Organization Collaboration Baseline (Candidate)

[简体中文](../COLLABORATION_BASELINE.md) · **English** · [Français](COLLABORATION_BASELINE.fr.md) · [Español](COLLABORATION_BASELINE.es.md) · [Русский](COLLABORATION_BASELINE.ru.md)

> Status: `PROPOSED` · Scope: the organization's public `.github` repository · Stewardship: organization owner or designated maintainers.
>
> This describes the **scope and activation conditions** of default community health templates. It is not a product Canonical specification, an approved technical ADR, an organization permission setting or proof that a security audit was executed.

## Purpose and files

Help contributors across repositories submit issues, discuss changes, open PRs and coordinate security reports consistently and with verifiable evidence, while preserving each project's control over its code, specifications, CI and releases.

| File | Purpose | Boundary |
| --- | --- | --- |
| [CONTRIBUTING.md](CONTRIBUTING.en.md) | Collaboration, confidentiality and evidence | Does not promise acceptance of external contributions |
| [PULL_REQUEST_TEMPLATE.md](../../PULL_REQUEST_TEMPLATE.md) | Scope, authorization, risks, verification and HOLD | Does not replace required checks or review |
| [bug_report.yml](../../.github/ISSUE_TEMPLATE/bug_report.yml) | Reproduction and defect evidence | No sensitive exploit details in public |
| [change_proposal.yml](../../.github/ISSUE_TEMPLATE/change_proposal.yml) | Engineering, research and governance proposals | A proposal is not an adopted standard |
| [config.yml](../../.github/ISSUE_TEMPLATE/config.yml) | Keeps blank Issues available | Repository-specific configuration may override it |
| [SECURITY.md](SECURITY.en.md) | Responsible disclosure | Does not invent private reporting channels or SLAs |

## Inheritance, activation and local precedence

GitHub supports default community health files from an organization's **public `.github` repository on its default branch**. Eligible files may be inherited by **public and private** organization repositories that do not supply their own equivalent files. A repository-local file takes precedence. Templates alone do not enforce permissions, branch protection or approvals.

While this package exists only on a separate branch in a **Draft PR**, its contents are **proposed, not activated**. Inheritance may begin only when eligible files are merged into the public `.github` default branch. The actual outcome also depends on local overrides. Creating an `AGENTS.md` in the organization `.github` repository does not automatically distribute agent instructions; agents must read the instructions, knowledge, specifications and ADRs actually applicable to each target repository.

## Authority and evidence semantics

1. Approved ecosystem and project rules, ADRs, code, migrations, tests and commit-bound implementation facts remain owned by their respective repositories.
2. Keep `target / implementation / gap` separate. A design target does not prove implementation, and existing code does not imply acceptance.
3. Distinguish `PROPOSED / ACCEPTED / IMPLEMENTED / STATIC_VERIFIED / LOCAL_PASS / REMOTE_CI_PASS / UNVERIFIED / BLOCKED / HOLD`. Report a check that was not performed as `NOT RUN`, not `PASS`.
4. Chat, Codex or local Linux validation may be engineering evidence when its environment and raw results are identified. It is not a native GitHub Actions Check. CI, quota and billing blockers must be recorded separately from source-code failures or successful checks.
5. Private repository contents, unreleased research, access settings and raw security audit data remain confidential despite the templates' location in a public repository.

## Checks before activation — owner/maintainer decision required

- [ ] Review all public wording and confirm it contains no private or unapproved facts.
- [ ] Confirm a real confidential vulnerability-reporting route. Any email address or Private Vulnerability Reporting feature must be chosen and configured, not invented.
- [ ] Check inheritance and repository-local overrides in both public and private target repositories; otherwise mark `NOT VERIFIED`.
- [ ] Verify both Issue Forms render correctly in GitHub, including required fields and safety warnings; otherwise mark `NOT VERIFIED`.
- [ ] Confirm that repository instructions, review, CI, exact HEAD, HOLD and release gates remain intact.
- [ ] Obtain explicit owner approval for cross-repository default activation before moving the Draft PR toward merge, then follow the applicable review and merge policy.
