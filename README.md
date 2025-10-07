# Cleopatra UMG Operations Workspace

This private repository captures ongoing automation, analytics, and research work for Universal Music Group (UMG). It is designed to stay organized as we add tools for monitoring domains, managing marketing data, and producing internal reports.

## Repository Structure

- `automated_testing/`
  - `lighthouse/`: Scripts and configuration for performance audits with Google Lighthouse.
  - `statusup/`: Status and uptime checker workflows.
- `db/`: Shared SQLite storage that every tool in this repository must use.
- `google_api/`: CLI utilities for connecting to, visualizing, and manipulating Google Ads, Analytics, and GTM data.
- `reports/`: Generated outputs, dashboards, and status summaries.
- `research/`: Notes, findings, and background investigations that inform UMG initiatives.
- `spec/`
  - `gtm_configs/`: Specification files for GTM container setups and deployment playbooks.
- `umg_domains.csv`: Canonical list of UMG domains and associated metadata (entity type, region, notes).

Keep this file updated as new folders and tooling are introduced so contributors have a single source of truth for the workspace layout.

## Shared Database Convention

All applications and scripts that persist structured data must write to the shared SQLite database located in the `db/` directory. Extend its schema as needed, but do not create alternate database files elsewhere in the project tree.

## Getting Started

1. Review the `AGENTS.md` file for collaboration guidelines.
2. Populate `db/` with the shared SQLite database file when you introduce the first tool that requires persistence.
3. Use the `umg_domains.csv` file as the master inventory of domains when building monitoring or analytics automations.
