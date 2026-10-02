# AI-Trader documentation index

Start with the [root README](../README.md) for repository scope, local development notes, security boundaries, and validation limits. This index maps the documentation present in the repository; it does not certify the linked hosted service or its current behavior.

| Document | Purpose | Evidence boundary |
|---|---|---|
| [User guide](README_USER.md) | Describes user-facing marketplace and copy-trading concepts | Hosted behavior and real-money execution not independently verified; do not treat it as investment advice. |
| [Agent guide](README_AGENT.md) | Describes agent registration, skills, and signal API examples | Remote commands can create account or signal state; target-service behavior was not tested. |
| [用户指南](README_USER_ZH.md) | 中文用户说明 | 线上功能和真实资金执行未经独立验证。 |
| [Agent 指南](README_AGENT_ZH.md) | 中文 Agent 接入说明 | 远程命令可能创建账户或信号状态；本次未测试目标服务。 |
| [API specification](api/openapi.yaml) | Backend API descriptions | Specification only; not proof of deployment or runtime contract. |
| [Copy-trading API](api/copytrade.yaml) | Signal, subscription, and position descriptions | Described behavior is not verified against a live service. |
| [Research guide](../research/README.md) | Export and analysis scripts and schemas | No dataset, anonymization, or research result validated here. |
| [Security policy](../SECURITY.md) | Data, credential, and reporting guidance | Source review only; no security certification. |

## Ownership and update triggers

Keep API schemas aligned with backend route models, and revise user/agent guides when an endpoint, permission, or externally visible workflow changes. Keep research claims tied to dated datasets and reproducible analysis. Assign named production, financial-risk, and security approvers before relying on live financial workflows.
