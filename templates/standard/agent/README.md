# Agent Workspace

Este diretório concentra o material de trabalho do agente sem poluir a raiz do repositório.

## Entradas úteis

- [../agent-start-here.md](../agent-start-here.md)
- [policy/README.md](./policy/README.md)
- [specs/README.md](./specs/README.md)
- [../docs/README.md](../docs/README.md)
- [specs/project.spec.md](./specs/project.spec.md)
- [specs/project.stat.md](./specs/project.stat.md)

## Estrutura

- `policy/`
  - regras duráveis para trabalho do agente;
  - convenções de fluxo, contrato, documentação e segurança.
- `specs/`
  - especificações normativas;
  - status de andamento;
  - pares `.spec` / `.stat`.
- `prints/`
  - capturas de tela;
  - imagens temporárias de apoio;
  - comparações visuais.
- `tmp/`
  - prints de teste;
  - capturas temporárias;
  - artefatos descartáveis.
- `reports/`
  - relatórios curtos de validação;
  - sumários de auditoria;
  - saídas que merecem ficar organizadas.
- `scripts/`
  - scripts auxiliares e automações curtas;
  - utilitários de teste.
- `test/`
  - testes pontuais e verificações de apoio;
  - rascunhos de validação.
- `note/`
  - anotações mais íntimas do agente;
  - rascunhos de raciocínio;
  - observações de contexto.

## Regras

- mantenha o resto do repositório limpo;
- não use a raiz para prints e rascunhos;
- promova para documentação oficial apenas o que estiver estável;
- não guardar segredos, tokens, dumps ou dados sensíveis sem motivo explícito.

## Relacionados

- [../agent-start-here.md](../agent-start-here.md)
- [../docs/README.md](../docs/README.md)
