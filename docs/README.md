# Documentation index

This index links to files present in the repository tree. Descriptions in guides and API specs are not independent proof that a hosted service is available.

## Start here

- [Project README](../README.md)
- [Chinese README](../README_ZH.md)
- [Agent guide](README_AGENT.md)
- [User guide](README_USER.md)
- [Backend service notes](../service/README.md)

## API and agent workflows

- [Backend API specification](api/openapi.yaml)
- [Copy trading API specification](api/copytrade.yaml)
- [AI-Trader skill](../skills/ai4trade/SKILL.md)
- [Copy trading skill](../skills/copytrade/SKILL.md)
- [Trade sync skill](../skills/tradesync/SKILL.md)
- [Market intelligence skill](../skills/market-intel/SKILL.md)
- [Polymarket skill](../skills/polymarket/SKILL.md)
- [Heartbeat skill](../skills/heartbeat/SKILL.md)

## Research

- [Research tools and data boundaries](../research/README.md)
- [Research process log](../research/experiment_process_log.md)
- [Research schemas](../research/schemas/)

## Current verification boundary

This repository contains application source, API specifications, agent instruction files, research scripts, and schemas. This documentation pass does not verify hosted endpoint availability, live market or broker integrations, real-money execution, production data, test results, or investment performance. No root license file was present on the inspected default branch as of 2026-10-02.

The agent guide references a Marketplace Seller skill at `skills/marketplace/SKILL.md`, but that file was not present in the inspected tree. Use the existing `skills/ai4trade/SKILL.md` guide until the missing path is corrected.