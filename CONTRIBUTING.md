# Contributing to PROTORHEXIS / 参与源爆点协作

欢迎以问题报告、研究线索、设计讨论、文档改进或代码变更参与源爆点（PROTORHEXIS）。我们重视清楚的边界、可追溯的判断和彼此尊重的协作。本文件是组织的**默认协作指南**，不代表所有仓库都开放外部贡献，也不构成对研究、实现或发布状态的承诺。

## 1. 先确认仓库与权限 / Start with repository scope

1. 阅读目标仓库的 `README.md`、`CONTRIBUTING.md`、`AGENTS.md`、安全政策、贡献限制和相关任务说明（如果存在）。
2. 确认该仓库是否接受 Issue、Pull Request 或外部贡献。私有仓库的内容、存在性、配置和访问权限均不得因为参与组织协作而对外披露。
3. 目标仓库的具体指南、已批准的规范与 ADR、维护者决定、保护分支及既有审批门禁优先于本文的通用建议。若要求冲突，说明冲突并请求维护者裁决；不要自行降低更高权威规则。
4. 开始前先搜索既有 Issue/PR，避免重复。对于显著改变架构、接口、治理、数据处理或公共承诺的事项，先提出方案并等待范围确认。

## 2. 提交有上下文的变更 / Make changes reviewable

- Issue 说明观察到的行为、预期行为、复现条件、影响范围和已知证据；推测必须标为推测。
- PR 尽量聚焦单一意图，交代变更目的、影响仓库或契约、测试与验证范围、兼容性、风险与回退办法。
- 区分目标设计、已经实现的事实与尚未满足的差距。未经执行的检查写为 `NOT RUN` 或 `UNVERIFIED`，不能写为 PASS。
- 对声称验证通过的结论给出执行环境、命令、结果及对应源码提交。局部或本地验证不等于远程 CI、部署资格或发布批准。
- 避免顺手重命名、重排或删除无关内容。涉及数据迁移、权限修改、破坏性操作、敏感信息或跨项目契约时，先取得适用的明确授权。
- 不上传密钥、Token、个人敏感信息、内部运行日志、私有代码摘录或未经允许公开的研究材料。发现漏洞请按 [Security Policy](SECURITY.md) 协调私密披露。

## 3. 审查与状态 / Review and status

使用 PR 模板说明当前状态，例如 `PROPOSED`、`IMPLEMENTED`、`STATIC_VERIFIED`、`LOCAL_PASS`、`REMOTE_CI_PASS`、`UNVERIFIED`、`BLOCKED` 或 `HOLD`。这些标签描述不同证据层次，不可互相替代。

提交 PR 不等于已经获批。维护者依据目标仓库的实际审批、Required Checks、准确 HEAD、评审和发布规则决定是否合并。任何 `HOLD`、冻结约束或受控发布门都不会因本文或一次普通 PR 自动解除。

## 4. 行为准则 / Collaboration conduct

请对人保持尊重，对论点保持严格。欢迎跨学科分歧、可复现的反例和善意纠错；拒绝骚扰、歧视、泄露私人资料或以人身攻击替代证据。若出现不当行为，请优先通过目标仓库维护者可用的适当渠道反馈，避免在公开讨论中扩散当事人的私密信息。

## English summary

This is a default guide, not an invitation to access private repositories or an organization-wide approval policy. Read repository-specific instructions first; propose consequential changes before implementation; keep PRs focused; attach reproducible, commit-bound evidence; distinguish design, implementation, verification and release readiness; and protect confidential information. Existing reviews, required checks and HOLD decisions remain in force.
