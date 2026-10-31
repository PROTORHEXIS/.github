# PROTORHEXIS 组织协作基线（候选）

> Status: `PROPOSED` · 适用对象：组织公共 `.github` 仓库 · 维护：组织 Owner/指定维护者
>
> 本文说明通用模板的**适用范围与启用条件**，不是产品 Canonical、技术 ADR、仓库权限设置或已执行的安全审计证明。

## 目标

让不同仓库的贡献者能够以一致、清楚、可核验的方式提出问题、讨论变更、提交 PR 和协调安全漏洞，同时保留各项目对代码、规范、CI 和发布的独立控制权。

本候选包包含：

| 文件 | 用途 | 约束边界 |
| --- | --- | --- |
| [`CONTRIBUTING.md`](../CONTRIBUTING.md) | 通用参与规范与证据语言 | 不承诺接受外部贡献 |
| [`PULL_REQUEST_TEMPLATE.md`](../PULL_REQUEST_TEMPLATE.md) | 摘要、影响、授权、验证、HOLD | 不替代 Required Checks 或 Review |
| [`bug_report.yml`](../.github/ISSUE_TEMPLATE/bug_report.yml) | 缺陷证据与复现 | 禁止公开敏感安全细节 |
| [`change_proposal.yml`](../.github/ISSUE_TEMPLATE/change_proposal.yml) | 候选工程、研究与治理提案 | 提案不是已批准规范 |
| [`config.yml`](../.github/ISSUE_TEMPLATE/config.yml) | 保留自由格式 Issue 入口 | 各项目可覆盖 |
| [`SECURITY.md`](../SECURITY.md) | 负责任的漏洞披露引导 | 不声称私密报告已启用或提供 SLA |

## 继承范围、启用方式与覆盖规则

GitHub 会从组织的**公开 `.github` 仓库默认分支**向缺少对应文件的组织仓库提供受支持的社区健康文件，适用于公共及私有仓库。目标仓库拥有自己的同类文件时，以目标仓库的版本为准。默认模板不是 GitHub 权限、分支保护或强制审批的技术门禁。

因此，本包在**独立分支和 Draft PR** 中只属于候选内容。只有审查通过并**合并到 `.github` 的默认分支**后，受支持的默认文件才可能被其他仓库继承；继承效果还取决于目标仓库是否已有自己的同类模板。不要将 Draft PR 或文件创建视为组织范围内已启用。

组织 `.github` 仓库不会让 `AGENTS.md` 自动继承到所有子仓库。Agent 应进入目标仓库，读取其自身的 `AGENTS.md`、`CLAUDE.md` 和实际适用的知识、规范、ADR，再决定任务授权及执行流程。组织模板仅收集协作证据，不成为更高权威规则。

## 权威与状态语义

1. 已批准的生态与项目规范、ADR，以及项目代码、测试和提交绑定的实现事实，仍由其各自仓库维护；组织模板不复制或取代它们。
2. 保留 `target / implementation / gap` 的区分。目标规范不等于已实现；代码存在也不代表通过验收。
3. 保留 `PROPOSED / ACCEPTED / IMPLEMENTED / STATIC_VERIFIED / LOCAL_PASS / REMOTE_CI_PASS / UNVERIFIED / BLOCKED / HOLD` 的区分。使用实际检查结果和准确的执行提交，未经执行即标 `NOT RUN`。
4. Chat、Codex 或本地 Linux 验证可构成注明来源的工程证据，但不伪装为 GitHub Actions Check。任何 CI 配额/计费阻断应单独记录，不构成源码测试失败或 PASS。
5. 任何私有仓库内容、未公开研发成果、权限配置和安全审计原始信息不因模板位于公开仓库而变成可公开材料。

## 启用前检查（需要 Owner/维护者裁决）

- [ ] 逐项审阅公开内容；确认没有私人信息或未批准公开的项目事实。
- [ ] 明确 `SECURITY.md` 中的安全联系路径是否足够；如需指定邮箱或启用 Private Vulnerability Reporting，先由 Owner 决定和配置，不要虚构入口。
- [ ] 在公共及私有目标仓库分别检查默认文件是否被继承，且已有本地模板能够覆盖；没有执行时标记 `NOT VERIFIED`。
- [ ] 检查两个 Issue Form 的 GitHub 实际渲染、字段必填与安全提示；没有执行时标记 `NOT VERIFIED`。
- [ ] 确认目标仓库的审批、CI、准确 HEAD、HOLD、发布和 Agent 指令不受默示改写。
- [ ] 只有在明确批准跨仓库默认生效的影响之后，才可将 Draft PR 转为可合并并完成适用评审；本文件本身不授予合并权限。

## English overview

This is a **candidate** set of default community health files for the organization’s public `.github` repository. On merge to the default branch, eligible files may be inherited by organization repositories—including private repositories—that lack local equivalents. Repository-specific files override defaults. The templates collect context and evidence, but do not establish branch protections, override local agent instructions, grant merge or release permission, or clear existing HOLD states. Security contacts and live rendering/inheritance must be checked before activation.
