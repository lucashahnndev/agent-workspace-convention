# agent-workspace-convention

A lightweight convention for organizing agent work in projects.

If you are an agent, start with `AGENTS.md`.
If you are human, copy the prompt below and send it to your agent.

Convention metadata lives in `awc.meta.toon`.

In target projects, `README.md` stays as the human landing page and
`project.overview.md` becomes the root overview for agent-oriented navigation.

## Prompt for the agent

Use this prompt to install the convention:

```text
Read first:

https://raw.githubusercontent.com/lucashahnndev/agent-workspace-convention/main/AGENTS.md

Then apply the `standard` convention to this project.

Before any commit, show me:
- created files;
- `git status --short`;
- any doubts or conflicts found.
```

## Adequation

Use this prompt when the convention is already installed and you want to start
the adequation pass:

```text
Read `AGENTS.md`.
Then read `project.update.md`.
Follow the adequation roadmap in `agent-start-here.md`.
Then execute the adequation phases described in `AGENTS.md`.

Before any commit, show me:
- inventory;
- created files;
- changed files;
- `git status --short`;
- any doubts or conflicts found.
```

## Update the convention

Use this prompt to update a project that is already using the convention, that is, when
the local installation diverges from the version registered in `awc.meta.toon`:

```text
Read the convention source `AGENTS.md`:
https://raw.githubusercontent.com/lucashahnndev/agent-workspace-convention/main/AGENTS.md
Then read `project.update.md`.
If the project needs multiple upgrade steps, also read `project.migrations.md`.

If the local installation diverges from the SemVer version in `awc.meta.toon`,
reapply `standard` and align only the convention files. Then read
`agent-start-here.md` and follow the adequation roadmap.

Before any commit, show me:
- trace_id;
- created files;
- changed files;
- `git status --short`;
- doubts.
```
