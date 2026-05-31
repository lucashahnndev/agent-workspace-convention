# agent-workspace-convention

Uma convenção leve para organizar o trabalho de agentes em projetos.

Se você for um agente, comece por `AGENTS.md`.
Se você for humano, copie o prompt abaixo e envie para o seu agente.

Os metadados da convenção vivem em `awc.meta.toon`.

## Para humanos

Este repositório é a fonte da convenção. Ele reúne uma forma simples de organizar entrada, contrato, andamento e workspace de agentes.

O conteúdo em `templates/standard/` é o template copiável para projetos alvo. Ao aplicar esse template, o projeto destino recebe `agent-start-here.md`, `agent/specs/`, `agent/policy/` e o workspace operacional esperado.

O repositório-fonte não é um projeto alvo por padrão e não precisa ser dogfoodado na raiz neste momento.

Se você quer aplicar a convenção em um projeto, o caminho é:

1. copiar o template `standard`;
2. pedir ao agente para ler `agent-start-here.md`;
3. deixar o agente seguir a convenção do projeto alvo.

## Prompt para o agente

Use este prompt para aplicar a convenção:

```text
Leia primeiro `AGENTS.md` da convenção.
Depois aplique `standard` neste projeto.
Use `trace_id` antes do commit e me mostre `trace_id`, arquivos criados, arquivos alterados, `git status --short` e dúvidas.
```

## Atualizar a convenção

Use este prompt para atualizar um projeto já convencionado:

```text
Leia primeiro `AGENTS.md` da convenção.
Atualize este projeto para a versão registrada em `awc.meta.toon`.
Sincronize apenas os arquivos da convenção com `templates/standard/`.
Preserve alterações fora do escopo da convenção.
Use `trace_id` antes do commit e me mostre `trace_id`, arquivos criados ou alterados, `git status --short` e dúvidas.
```

## Onde olhar

- `AGENTS.md`: instruções para agentes;
- `awc.meta.toon`: metadados da convenção;
- `templates/standard/`: template inicial para um projeto alvo.
