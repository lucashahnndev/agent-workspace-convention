# Agent Start Here

Este é o ponto de entrada do agente neste projeto.

Leia este arquivo primeiro.
Depois siga a ordem abaixo.

## Ordem de leitura

1. `README.md` do projeto.
2. `.spec` relevante em `agent/specs/`, incluindo specs de sistema, arquitetura, contrato ou domínio que governem a mudança.
3. `.stat` correspondente.
4. documentação humana, operacional ou de arquitetura relevante em `docs/`, quando existir.
5. testes relacionados.

## Regra básica

- `.spec` é contrato durável.
- `.stat` é estado vivo.
- `agent/` é workspace operacional.
- as regras detalhadas ficam em [agent/policy/README.md](agent/policy/README.md).

## Regra de abstração

Se o tema parecer amplo o suficiente para virar contrato, verifique primeiro se já existe uma `.spec` parecida.
Se houver conflito, ajuste a proposta antes de criar nova documentação.
Se fizer sentido formalizar, crie uma `.spec` com nome abstrato e estável.

## Regra de trabalho

- mantenha mudanças pequenas e coerentes;
- valide antes de avançar;
- registre evidência no workspace apropriado;
- ligue documentos relevantes quando isso ajudar a entender contrato, dependência ou continuidade;
- quando o alvo for um arquivo que não é `.md`, use referência explícita ao arquivo ou caminho exato; não crie nota nova para representá-lo;
- não reorganize arquivos existentes sem aprovação;
- atualize `.stat` quando houver progresso real;
- atualize docs oficiais apenas quando contrato ou uso mudar.
- para commits, siga [agent/policy/commit-safety.policy](agent/policy/commit-safety.policy.md) e use `trace_id` quando houver mudança relevante.

## Protocolo de adequação

Quando este repositório já recebeu a convenção e precisa ser alinhado ao padrão:

1. aplique o bootstrap da convenção;
2. ajuste `graph.json` e as exclusões do vault;
3. faça inventário de artefatos, arquivos soltos e ruído operacional;
4. peça aprovação antes de organizar, mover ou apagar;
5. organize o repositório;
6. mapeie documentação que precisa virar contrato, estado ou doc oficial;
7. proponha e, depois de aprovado, crie ou ajuste `.spec`, `.stat` e links;
8. consolide com `trace_id` e deixe a `.stat` rastreável.

Depois do bootstrap, use a mensagem padrao de handoff da policy de adequacao
e peça aprovacao para iniciar a fase seguinte.

Se houver dúvida sobre a próxima etapa, siga [agent/policy/adequation.policy.md](agent/policy/adequation.policy.md).

## Relacionados

- [agent/specs/README.md](agent/specs/README.md)
- [agent/policy/README.md](agent/policy/README.md)
