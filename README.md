# agent-workspace-convention

Uma convenção leve para organizar o trabalho de agentes em projetos.

## Para humanos

Este repositório reúne uma forma simples de organizar entrada, contrato, andamento e workspace de agentes.

Se você quer aplicar a convenção em um projeto, o caminho é:

1. copiar o template `standard`;
2. pedir ao agente para ler `agent-start-here.md`;
3. deixar o agente seguir a convenção do projeto alvo.

## Para começar com um agente

Use este prompt:

```text
Leia o arquivo agent-start-here.md primeiro.
Depois leia a .spec relevante e a .stat correspondente.
.spec é contrato durável; .stat é estado vivo.
Se o tema parecer merecer uma nova spec, verifique primeiro se já existe algo parecido.
Não use documentação normativa como diário de progresso.
Registre andamento na .stat e evidência no workspace apropriado.
```

## Onde olhar

- `AGENTS.md`: instruções para agentes;
- `templates/standard/`: template inicial para um projeto alvo.
