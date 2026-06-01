# Specs

This directory stores the target project's normative contracts that the agent must read and obey when changing the system.

## Rules

- every active `.spec` must have a `.stat`;
- `.spec` defines durable contract;
- `.stat` records live state;
- do not use `.spec` as a progress log;
- do not use `.stat` to redefine contract;
- this includes system, architecture, product behavior, module contracts, domain rules, and operational policies;
- `docs/` is official human-facing documentation and may reference specs, but it is not the main place for normative contract.

## Convention

- `nome-do-dominio.spec.md`
- `nome-do-dominio.stat.md`

## Initial base

- `project.spec.md`
- `project.stat.md`

## Related

- [../policy/overview.md](../policy/overview.md)
