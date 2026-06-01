# Project Migrations

This ledger records version-to-version changes for AWC installations.
Legacy versions may appear in the `vN` format; the current SemVer baseline is
`0.0.1`.

## How to use

1. Read `awc.meta.toon` and identify the installed version.
2. Open this ledger and find the next applicable migration row.
3. Apply the listed change set.
4. Re-read `awc.meta.toon` and continue until the installed version matches the
   convention version.
5. Use SemVer ordering from `0.0.1` onward.

## Migration ledger

| From | To | Purpose | Files to review | Main action | Notes |
|------|----|---------|-----------------|-------------|-------|
| v4 | v5 | translate the convention source to English | `README.md`, `AGENTS.md`, `templates/standard/` | translate human-facing text while preserving structure and links | source language becomes `en` |
| v5 | v6 | add `project.overview.md` as the root agent map | `project.overview.md`, `agent-start-here.md`, `AGENTS.md` | create the agent-oriented root overview and route the agent through it | human `README.md` stays human |
| v6 | v7 | replace internal `README.md` indexes with `overview.md` | `agent/`, `docs/`, `agent/policy/`, `agent/specs/`, `docs/*` | rename internal folder indexes to `overview.md` and keep the root landing page human | reduces `README` collisions in the graph |
| v7 | v8 | add `project.update.md` and version-aware update flow | `project.update.md`, `README.md`, `AGENTS.md`, `agent-start-here.md` | create the update index, compare against `awc.meta.toon`, and route updates through the new flow | update path becomes explicit and reusable |
| v8 | v9 | add `project.migrations.md` and version-by-version update flow | `project.update.md`, `project.migrations.md`, `README.md`, `AGENTS.md` | create the migration ledger, compare the installed version with `awc.meta.toon`, and replay one migration row at a time | updates can now step through multiple versions |
| v9 | 0.0.1 | migrate the convention metadata to SemVer | `awc.meta.toon`, `README.md`, `AGENTS.md`, `project.update.md`, `project.migrations.md` | change the version field to semantic versioning and keep the legacy `vN` rows as historical context | `0.0.1` is the first SemVer baseline |

## Update pattern

- use one row at a time;
- do not skip a version if the local installation still depends on it;
- if a project already matches a row, continue to the next one;
- ask for approval before moving, deleting, or consolidating structural files.

## Related

- [project.update.md](project.update.md)
- [project.overview.md](project.overview.md)
- [AGENTS.md](AGENTS.md)
