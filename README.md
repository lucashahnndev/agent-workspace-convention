# agent-workspace-convention

Uma convenção leve para organizar o trabalho de agentes em projetos.

Se você for um agente, comece por `AGENTS.md`.
Se você for humano, copie o prompt abaixo e envie para o seu agente.

Os metadados da convenção vivem em `awc.meta.toon`.

## Prompt para o agente

Use este prompt para aplicar a convenção:

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

Use este prompt para atualizar um projeto já convencionado, ou seja, quando a
instalação local divergir da versão registrada em `awc.meta.toon`:

```text
[MODE] update
[READ] [AGENTS.md](AGENTS.md)
[COND] local-version != [awc.meta.toon](awc.meta.toon)
[APPLY] [standard](templates/standard/)
[READ] [agent-start-here.md](templates/standard/agent-start-here.md)
[FLOW] adequation-roadmap
[REPORT] trace_id | created-files | changed-files | git-status-short | doubts
```
