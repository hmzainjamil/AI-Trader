# AI-Trader

面向 AI Agent 的交易信号与研究应用代码库，包含 FastAPI 后端、React/Vite 网页客户端、Agent 技能说明、API 规范和研究分析脚本。

> **状态：** 开发中的代码库。本次只检查了源代码目录结构；没有验证运行结果、外部服务可用性、部署状态、真实交易执行或财务表现。

仓库公开可见不代表允许复用。截至 2026-10-02，本次检查的默认分支中没有根目录 `LICENSE` 文件。

## 项目范围

代码中包含 Agent 注册、信号、市场数据、交易相关路由、挑战赛、实验、团队任务和研究导出模块。源代码或 API 规范的存在，不代表功能已经部署、线上服务可用，或可用于真实资金交易。

本项目不作收益、盈利能力、执行质量或未来表现的承诺。不要仅凭本说明连接真实资金或凭证。

## 组成部分

| 部分 | 路径 | 证据边界 |
|---|---|---|
| FastAPI 应用 | `service/server/` | 已检查源码；本次未运行 |
| React/Vite 客户端 | `service/frontend/` | 已检查依赖脚本和源码目录；本次未构建 |
| Agent 技能说明 | `skills/` | Markdown 操作说明，不证明线上功能可用 |
| API 描述 | `docs/api/` | API 规范，不证明线上端点已部署 |
| 研究工具与数据结构 | `research/` | 脚本和数据结构定义；本次未验证数据集或结果 |

## 本地开发

以下命令依据仓库中的依赖清单和应用入口整理，本次未执行。

启动后端：

```sh
python -m venv .venv
source .venv/bin/activate
python -m pip install -r service/requirements.txt
python -m uvicorn main:app --app-dir service/server --reload
```

应用默认按本地开发配置使用 8000 端口。未设置 `DATABASE_URL` 时，代码默认使用 SQLite；Redis 缓存为可选项。

另开终端启动前端：

```sh
cd service/frontend
npm install
npm run dev
```

Vite 配置使用 3000 端口。请按实际环境配置 CORS 和第三方服务。后端从 `service/.env` 读取环境变量；根目录的 `.env.example` 仅供查看变量名称和说明。使用前请先审查，并将凭证放在 Git 忽略的本地文件中。不要提交真实密钥。

## 文档

请先阅读[文档索引](docs/README.md)，了解各指南的用途和证据边界。

- [文档索引](docs/README.md)
- [Agent 指南](docs/README_AGENT.md)
- [用户指南](docs/README_USER.md)
- [后端 API 规范](docs/api/openapi.yaml)
- [Copy trading API 规范](docs/api/copytrade.yaml)
- [Agent 技能说明](skills/ai4trade/SKILL.md)
- [研究工具说明](research/README.md)

## 安全、隐私与限制

- 将市场、账户、钱包和服务商数据视为敏感信息。
- API 规范和技能文件可能描述本仓库无法验证的行为。
- 对外部署前，请审查认证、授权、服务商访问、数据保留和风险控制。
- 本说明不声明安全、合规、生产就绪或真实交易认证。
- 仓库没有根目录许可证文件，复用条款未明确。

## 验证

本次 README 更新未运行测试、构建、部署或外部服务检查。发布前应运行仓库中的检查，并记录真实结果。