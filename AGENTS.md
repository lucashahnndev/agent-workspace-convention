# AGENTS.md

This file is for agents that will apply the convention in another project.

You are in the convention source repository, not a target project. Do not confuse the files in this repository with the files that will be copied into another workspace. When applying the convention, copy and adapt `templates/standard/` into the destination project. Do not dogfood the source repository on your own without explicit request.

The short alias for the convention is `awc`, short for `agent-workspace-convention`.

The version and control metadata live in `awc.meta.toon` at the repository root.
The current convention version uses SemVer starting at `0.0.1`.

## Goal

Provide a simple and stable base so agents can:

- find the entry point;
- separate contract from progress;
- keep documentation truthful;
- use an operational workspace without polluting the repository;
- continue work across sessions.

## Recommended structure

Copy `templates/standard/` into the target project.

The `standard` template creates:

- `project.overview.md`
- `project.update.md`
- `project.migrations.md`
- `agent-start-here.md`
- `agent/overview.md`
- `docs/overview.md`
- `docs/contracts/overview.md`
- `docs/policies/overview.md`
- `docs/reports/overview.md`
- `docs/plans/overview.md`
- `docs/guides/overview.md`
- `docs/decisions/overview.md`
- `docs/concepts/overview.md`
- `docs/legacy/overview.md`
- `.gitignore`
- `agent/policy/`
- `agent/specs/`
- `agent/tmp/.gitkeep`
- `agent/prints/.gitkeep`
- `agent/reports/.gitkeep`
- `agent/scripts/.gitkeep`
- `agent/test/.gitkeep`
- `agent/note/.gitkeep`

When the destination is also used as an Obsidian vault, the template includes the recommended graph profile in `templates/standard/.obsidian/graph.json`. This file is part of the convention's visual deployment and can be copied together with the rest of the template when the vault accepts the default configuration.

`README.md` remains the human landing page in target projects. `project.overview.md`
is the root overview for agent-oriented navigation.

`project.update.md` is the update index for projects that already have the
convention installed. It points the agent to the version metadata in
`awc.meta.toon` and to the adequation route when the local installation must be
reconciled with the convention.

`project.migrations.md` is the version-to-version migration ledger. It preserves
legacy `vN` rows for older installations and switches to SemVer for current and
future releases.

`project.migrations.md` is the version-to-version migration ledger. Use it when a
target project must step through multiple convention versions before it reaches
the current one.

In the default AWC visual profile, `README.md` and `AGENTS.md` must be treated as privileged entry nodes. They should stand out in the graph to guide the initial reading, because they usually appear spread across multiple repositories and work as cognitive entry doors for the convention.

When the vault is used for technical implementation inspection, it can be useful to copy the alternative profile in `templates/standard/.obsidian/graph-tech.json`. That profile is more discreet and separates code, configuration, tests, and documentation files without replacing the convention's main profile.

## Safe bootstrap

When applying the convention to a target project:

1. clone this repository into a temporary folder outside the target project;
2. copy only the contents of `templates/standard/`;
3. do not copy this repository's `.git` folder;
4. do not keep the convention clone inside the target project;
5. then read the `agent-start-here.md` created in the target project.

If the target project already has a `.gitignore`, merge the convention patterns with the project's existing patterns instead of deleting useful rules from the destination repository.

Example:

```bash
tmp_dir="$(mktemp -d)"
git clone https://github.com/lucashahnndev/agent-workspace-convention.git "$tmp_dir/agent-workspace-convention"
cp -R "$tmp_dir/agent-workspace-convention/templates/standard/." .
```

## Recommended Obsidian graph

When the target project uses Obsidian as a vault, apply the default profile in
`templates/standard/.obsidian/graph.json` and keep the following excluded as noise:

- `changelog` and `CHANGELOG`
- dependencies and build artifacts such as `node_modules`, `vendor`, `dist`, and `build`
- local environments such as `.venv`, `venv`, and `site-packages`
- vault configuration files and folders such as `.git` and `.obsidian`

If the location of these folders varies, configure **Excluded files** in Obsidian too, because that option hides files globally in Search, Graph View, and backlinks.

## Post-bootstrap: initial adequation

After applying `templates/standard/`, read the created `agent-start-here.md` and run `git status --short`. If there are modified files, untracked files, or operational noise, diagnose and classify each item as keep, investigate, move, rename, delete, or preserve. Do not delete, move, `reset`, `stash`, or commit without approval. Record the result of any approved adequation in the `.stat`.

## Detailed policy

The full rules live in `agent/policy/` in the target project.

This bootstrap only defines the map and the expected use.

## Working pattern

1. read `agent-start-here.md`;
2. read the relevant `.spec`;
3. read the corresponding `.stat`;
4. validate the impact;
5. update progress;
6. update official documentation only if behavior or contract changes;
7. leave the workspace clean.

## Expected flow when receiving the short prompt

When the agent receives the short prompt from `README.md`, it should treat
`AGENTS.md` as the source of detailed instructions and follow this route:

1. open the convention `AGENTS.md`;
2. identify whether the target project already has the convention installed or
   still needs `standard`;
3. if this is a new installation, clone the convention outside the target
   project and copy `templates/standard/` into the destination;
4. if it is an update, read `project.update.md`, then `project.migrations.md`,
   compare the local installation with `awc.meta.toon`, and reapply only the
   convention files that diverge for the next unapplied migration row;
5. read the created or updated `project.overview.md` in the target project;
6. read the created or updated `agent-start-here.md` in the target project;
7. follow the phased adequation protocol described in this file and in
   `adequation.policy.md`;
8. ask for approval before organizing, deleting, moving, or consolidating structural
   changes;
9. record relevant progress in `trace_id` and the corresponding `.stat`.

## Adequation protocol

When the convention is applied to a target project, the recommended flow is:

1. bootstrap the convention;
2. adjust `graph.json` and `.gitignore` for known local noise;
3. inventory artifacts, loose files, and temporary files;
4. ask for approval before organizing or deleting;
5. organize the repository;
6. map documentation that needs to become context, `.spec`, or `.stat`;
7. ask for approval before creating or moving contracts;
8. perform linking and consolidation;
9. update `.stat` with the real progress;
10. use `trace_id` to record the relevant change.

If context is missing for the next action, follow [templates/standard/agent/policy/adequation.policy.md](templates/standard/agent/policy/adequation.policy.md).
After the bootstrap, use the standard adequation handoff message and ask for approval before entering the next phase.
