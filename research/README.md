# Research and analysis tools

This directory contains scripts and schemas for exporting and analyzing AI-Trader application data. It does not contain validated study results or a bundled production dataset.

The export pipeline uses the backend research export module or CSV files generated through that module. The checked-in repository does not establish that a production database is available, authoritative, or populated with a particular number of agents. Treat any counts, performance results, and study conclusions as unverified until they are supported by a dated dataset and reproducible analysis.

## Workflows

Export a dataset:

```sh
python research/scripts/export_research_dataset.py --output-dir research/exports
```

Generate analysis tables from exported CSVs:

```sh
python research/scripts/analyze_experiments.py --input-dir research/exports --output-dir research/exports/tables
```

Generate figures:

```sh
python research/scripts/generate_figures.py --input-dir research/exports --tables-dir research/exports/tables --output-dir research/exports/figures
```

These commands are documented examples and were not executed in this README update. Review each script's current arguments and access controls before use.

## Data handling

The scripts and schemas describe export and analysis paths; they do not certify anonymization. Inspect generated files before sharing, especially when exports may contain agent IDs, names, free text, wallet or account data, tokens, or other identifiers. Keep private exports out of version control.

## Scripts and schemas

- `scripts/export_research_dataset.py`: exports research data.
- `scripts/build_agent_features.py`: derives agent-level features.
- `scripts/build_network_edges.py`: generates interaction-edge data.
- `scripts/compute_metrics.py`: computes analysis metrics.
- `scripts/analyze_experiments.py`: produces experiment analysis.
- `scripts/generate_figures.py`: generates figures.
- `schemas/`: database export schema definitions.

For repository setup, see the [root README](../README.md).