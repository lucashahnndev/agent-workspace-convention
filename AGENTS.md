# AGENTS.md

Este arquivo é voltado para agentes que vão aplicar a convenção em outro projeto.

## Objetivo

Fornecer uma base simples e estável para que agentes:

- encontrem o ponto de entrada;
- separar contrato de andamento;
- mantenham a documentação verdadeira;
- usem um workspace operacional sem poluir o repositório;
- consigam continuar o trabalho entre sessões.

## Estrutura recomendada

Copie `templates/standard/` para o projeto alvo.

O template `standard` cria:

- `agent-start-here.md`
- `agent/policy/`
- `agent/specs/`
- `agent/tmp/.gitkeep`
- `agent/prints/.gitkeep`
- `agent/reports/.gitkeep`
- `agent/scripts/.gitkeep`
- `agent/test/.gitkeep`
- `agent/note/.gitkeep`

## Política detalhada

As regras completas ficam em `agent/policy/` no projeto alvo.

O bootstrap aqui só define o mapa e o uso esperado.

## Forma de trabalhar

1. ler `agent-start-here.md`;
2. ler a `.spec` relevante;
3. ler a `.stat` correspondente;
4. validar o impacto;
5. atualizar andamento;
6. atualizar documentação oficial apenas se o comportamento ou contrato mudar;
7. deixar o workspace limpo.
