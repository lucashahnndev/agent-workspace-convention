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

Use este prompt:

```text
Leia primeiro:

https://raw.githubusercontent.com/lucashahnndev/agent-workspace-convention/main/AGENTS.md

Depois aplique a convenção `standard` neste projeto.

Antes de qualquer commit, me mostre:
- arquivos criados;
- `git status --short`;
- dúvidas ou conflitos encontrados.
```

## Atualizar a convenção

Use este prompt quando quiser atualizar um projeto já convencionado para a versão atual:

```text
Leia primeiro:

https://raw.githubusercontent.com/lucashahnndev/agent-workspace-convention/main/AGENTS.md

Atualize este projeto para a versão registrada em `awc.meta.toon`.

Sincronize apenas os arquivos da convenção com o template `templates/standard/`.

Preserve alterações fora do escopo da convenção.

Antes de qualquer commit, me mostre:
- arquivos criados ou alterados;
- `git status --short`;
- conflitos ou dúvidas encontradas.
```

## Onde olhar

- `AGENTS.md`: instruções para agentes;
- `awc.meta.toon`: metadados da convenção;
- `templates/standard/`: template inicial para um projeto alvo.
