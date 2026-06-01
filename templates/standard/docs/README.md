# Docs

Este diretório reúne a camada humana do projeto: explicação, contexto,
evidência, planejamento, decisão e legado.

## Índice

- [contracts/README.md](./contracts/README.md): documentação que explica contratos sem substituir a spec;
- [policies/README.md](./policies/README.md): documentação humana de governança e uso;
- [reports/README.md](./reports/README.md): evidência, auditoria e validação;
- [plans/README.md](./plans/README.md): migrações, fases e trabalho futuro;
- [guides/README.md](./guides/README.md): guias e playbooks operacionais;
- [decisions/README.md](./decisions/README.md): decisões aprovadas e fechadas;
- [concepts/README.md](./concepts/README.md): conceitos e modelos de evolução;
- [legacy/README.md](./legacy/README.md): histórico substituido ou fora da base ativa.

## Como ler

- use `docs/` para entender o contexto humano do projeto;
- use `agent/specs/` para ler o contrato normativo;
- use `agent/policy/` para ler as regras duráveis do agente;
- use `agent/README.md` para entender o workspace operacional;
- quando uma doc crescer a ponto de virar regra, considere migrar para
  `.spec` e `.stat`;
- quando uma doc citar um arquivo que nao seja `.md`, use o caminho explicito
  do arquivo; nao crie nota nova para representa-lo no Obsidian.

## Contratos relacionados

- [../agent/specs/README.md](../agent/specs/README.md)
- [../agent/specs/project.spec.md](../agent/specs/project.spec.md)
- [../agent/specs/project.stat.md](../agent/specs/project.stat.md)

## Relação com a convenção

- [../agent-start-here.md](../agent-start-here.md) é o ponto de entrada do agente;
- [../agent/policy/README.md](../agent/policy/README.md) concentra as policies duráveis;
- [../agent/specs/README.md](../agent/specs/README.md) concentra os contratos normativos;
- [../agent/README.md](../agent/README.md) concentra o workspace operacional;
- `docs/` complementa com contexto humano e continuidade conceitual;
- quando houver dúvida entre contrato e explicação, leia a spec correspondente primeiro.

## Relacionados

- [concepts/README.md](./concepts/README.md)
- [../agent/README.md](../agent/README.md)
