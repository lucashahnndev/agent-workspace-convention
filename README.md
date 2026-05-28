# agent-workspace-convention

Uma convenção leve para organizar o trabalho de agentes em projetos.

Se você for um agente, comece por `AGENTS.md`.
Se você for humano, copie o prompt abaixo e envie para o seu agente.

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

https://github.com/lucashahnndev/agent-workspace-convention/blob/main/AGENTS.md

Depois aplique a convenção `standard` neste projeto.

Antes de qualquer commit, me mostre:
- arquivos criados;
- `git status --short`;
- dúvidas ou conflitos encontrados.

Motivo:
o detalhe de clone, pasta temporária, cópia de template e aplicação segura deve ficar em AGENTS.md, não no README.
```

## Onde olhar

- `AGENTS.md`: instruções para agentes;
- `templates/standard/`: template inicial para um projeto alvo.
