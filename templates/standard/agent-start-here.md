# Agent Start Here

Leia este arquivo primeiro.

## Ordem de leitura

1. `README.md` do projeto.
2. `agent-start-here.md`.
3. `.spec` relevante em `agent/specs/`.
4. `.stat` correspondente.
5. documentação operacional e de arquitetura relevante.
6. testes relacionados.

## Regra básica

- `.spec` é contrato durável.
- `.stat` é estado vivo.
- `agent/` é workspace operacional.
- as regras detalhadas ficam em `agent/policy/`.

## Regra de abstração

Se o tema parecer amplo o suficiente para virar contrato, verifique primeiro se já existe uma `.spec` parecida.
Se houver conflito, ajuste a proposta antes de criar nova documentação.
Se fizer sentido formalizar, crie uma `.spec` com nome abstrato e estável.

## Regra de trabalho

- mantenha mudanças pequenas e coerentes;
- valide antes de avançar;
- registre evidência no workspace apropriado;
- atualize `.stat` quando houver progresso real;
- atualize docs oficiais apenas quando contrato ou uso mudar.
