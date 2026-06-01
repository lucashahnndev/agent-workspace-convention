# agent-workspace-convention

Uma convenção leve para organizar o trabalho de agentes em projetos.

Se você for um agente, comece por `AGENTS.md`.
Se você for humano, copie o prompt abaixo e envie para o seu agente.

Os metadados da convenção vivem em `awc.meta.toon`.

## Para humanos

Este repositório é a fonte da convenção. Ele reúne uma forma simples de organizar entrada, contrato, andamento e workspace de agentes.

O conteúdo em `templates/standard/` é o template copiável para projetos alvo. Ao aplicar esse template, o projeto destino recebe `agent-start-here.md`, `agent/README.md`, `docs/README.md`, a taxonomia de `docs/` (`concepts`, `contracts`, `policies`, `reports`, `plans`, `guides`, `decisions`, `legacy`), `agent/specs/`, `agent/policy/` e o workspace operacional esperado.

O repositório-fonte não é um projeto alvo por padrão e não precisa ser dogfoodado na raiz neste momento.

Se você quer aplicar a convenção em um projeto, o caminho é:

1. copiar o template `standard`;
2. pedir ao agente para ler `agent-start-here.md`;
3. deixar o agente seguir a convenção do projeto alvo.

## Prompt para o agente

Use este prompt para aplicar a convenção:

```text
Leia primeiro [AGENTS.md](AGENTS.md) da convenção.
Depois aplique `standard` neste projeto.
Use `trace_id` antes do commit e me mostre `trace_id`, arquivos criados, arquivos alterados, `git status --short` e dúvidas.
```

## Protocolo de adequação

Use este prompt quando o repositório já tem a convenção e você quer iniciar
a primeira rodada de adequação pós-instalação:

```text
Leia primeiro [AGENTS.md](AGENTS.md) da convenção.
Depois siga o protocolo de adequação em fases: bootstrap, ajustes de grafo e ignore, inventário, aprovação para organizar, organização, mapeamento de docs para .spec/.stat, aprovação para contexto e contratos, linkagem e consolidação.
Antes de mudar qualquer estrutura, mostre o inventário, os arquivos criados ou alterados, o `git status --short` e as dúvidas.
Use `trace_id` quando houver mudança relevante.
Depois do bootstrap, use a mensagem padrao de handoff da adequacao e peça aprovacao para iniciar a fase seguinte.
```

## Atualizar a convenção

Use este prompt para atualizar um projeto já convencionado, ou seja, quando a
instalação local divergir da versão registrada em `awc.meta.toon`:

```text
Leia [AGENTS.md](AGENTS.md). Se a versão local divergir de `awc.meta.toon`, reaplique `standard` e alinhe só os arquivos da convenção. Depois leia `agent-start-here.md` e siga o roadmap de adequação. Antes do commit, me mostre `trace_id`, arquivos criados, arquivos alterados, `git status --short` e dúvidas.
```

## Onde olhar

- `AGENTS.md`: instruções para agentes;
- `awc.meta.toon`: metadados da convenção;
- `templates/standard/`: template inicial para um projeto alvo.
