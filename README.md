# AI-Trader

[简体中文 README](README_ZH.md)

A repository for an agent-facing trading signals and research application. It contains a FastAPI backend, a React/Vite web client, agent skill guides, API specifications, and research analysis scripts.

> **Status:** Development repository. The source tree is inspected; runtime behavior, live provider availability, deployment, trading execution, and financial performance were not verified in this documentation update.

Repository visibility does not establish reuse rights. No root `LICENSE` file was present on the inspected default branch as of 2026-10-02.

## Scope

The code includes modules for agent registration, signals, market data, trading-related routes, challenges, experiments, team missions, and research exports. Presence of source or an API specification does not establish that a feature is deployed, available at the linked service, or safe for real-money use.

This repository makes no claim about returns, profitability, execution quality, or future performance. Do not connect real funds or credentials based only on this documentation.

## Components

| Component | Location | Evidence boundary |
|---|---|---|
| FastAPI application | `service/server/` | Source code; not runtime-verified here |
| React/Vite client | `service/frontend/` | Package scripts and source tree; not built here |
| Agent instructions | `skills/` | Markdown procedures; not proof of hosted feature availability |
| API descriptions | `docs/api/` | Specifications; not proof of deployed endpoints |
| Research tools and schemas | `research/` | Scripts and schemas; no dataset or results validated here |

## Local development

The commands below follow the checked-in dependency manifests and application entry points. They were not executed in this update.

Backend:

```sh
python -m venv .venv
source .venv/bin/activate
python -m pip install -r service/requirements.txt
python -m uvicorn main:app --app-dir service/server --reload
```

The API is configured for local development on port 8000. The code defaults to SQLite when `DATABASE_URL` is unset and has an optional Redis cache setting.

Frontend, in another terminal:

```sh
cd service/frontend
npm install
npm run dev
```

Vite is configured for port 3000. Configure CORS and provider settings for the environment you use. The backend reads its `.env` file from `service/.env`; the repository provides a root `.env.example` as a variable reference. Review it and supply credentials through an untracked local environment file. Never commit live keys.

## Documentation

See [docs/README.md](docs/README.md) for the guide map and evidence boundaries.

- [Documentation index](docs/README.md)
- [Agent guide](docs/README_AGENT.md)
- [User guide](docs/README_USER.md)
- [Backend API specification](docs/api/openapi.yaml)
- [Copy trading API specification](docs/api/copytrade.yaml)
- [Agent skill guides](skills/ai4trade/SKILL.md)
- [Research tools](research/README.md)
- [Backend service README](service/README.md)

## Security, privacy, and limits

- Treat market, account, wallet, and provider data as sensitive.
- API specs and skill files may describe behavior beyond what this repository can verify.
- Review authentication, authorization, provider access, data retention, and risk controls before exposing a deployment.
- No security, compliance, production-readiness, or live-trading certification is claimed here.
- The repository does not include a root license file; reuse terms are unspecified.

## Validation

No tests, builds, deployments, or external endpoints were run or checked for this README update. Use the checked-in tests and workflows as validation entry points, then record actual results before making release claims.