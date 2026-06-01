# Project Update

This is the update index for a project that already has AWC installed.

## Source of truth

- [awc.meta.toon](awc.meta.toon)
- [AGENTS.md](AGENTS.md)
- [project.overview.md](project.overview.md)
- [agent-start-here.md](agent-start-here.md)

## When to use

Use this file when the local installation may diverge from the convention version
recorded in `awc.meta.toon`.

## Update flow

1. Read `AGENTS.md`.
2. Compare the installed convention with `awc.meta.toon`.
3. Reapply `standard` only where the convention diverges.
4. Read `project.overview.md`.
5. Read `agent-start-here.md`.
6. Follow the adequation protocol before moving, deleting, or consolidating files.
7. Keep human `README.md` files in place when they are meant for people; add or
   rename `overview.md` for agent-oriented navigation.

## Documentation rule

- `README.md` stays as the human landing page.
- `overview.md` is the default agent-oriented index inside folders.
- if a folder needs both human and agent entry points, keep the human
  `README.md` and add `overview.md` alongside it.
- if a `README.md` is only an internal index, prefer replacing it with
  `overview.md`.

## Related

- [project.overview.md](project.overview.md)
- [agent-start-here.md](agent-start-here.md)
- [agent/overview.md](agent/overview.md)
- [docs/overview.md](docs/overview.md)
