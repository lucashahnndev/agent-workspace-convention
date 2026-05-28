# AGENTS.md

Este arquivo é voltado para agentes que vão aplicar a convenção em outro projeto.

Você está no repositório-fonte da convenção, não em um projeto alvo. Não confunda arquivos deste repositório com os arquivos que serão copiados para outro workspace. Ao aplicar a convenção, copie e adapte `templates/standard/` para o projeto destino. Não faça dogfood do repositório-fonte por conta própria sem pedido explícito.

## Objetivo

Fornecer uma base simples e estável para que agentes:

- encontrem o ponto de entrada;
- separem contrato de andamento;
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

## Bootstrap seguro

Ao aplicar a convenção em um projeto alvo:

1. clone este repositório em uma pasta temporária fora do projeto alvo;
2. copie apenas o conteúdo de `templates/standard/`;
3. não copie a pasta `.git` deste repositório;
4. não mantenha o clone da convenção dentro do projeto alvo;
5. depois leia o `agent-start-here.md` criado no projeto alvo.

Exemplo:

```bash
tmp_dir="$(mktemp -d)"
git clone https://github.com/lucashahnndev/agent-workspace-convention.git "$tmp_dir/agent-workspace-convention"
cp -R "$tmp_dir/agent-workspace-convention/templates/standard/." .
```

## Pós-bootstrap: higiene inicial

Depois de aplicar `templates/standard/`, leia o `agent-start-here.md` criado e rode `git status --short`. Se houver arquivos modificados, untracked ou bagunça operacional, faça um diagnóstico e classifique cada item em manter, investigar, mover, renomear, apagar ou preservar. Não apague, mova, faça `reset`, `stash` ou commit sem aprovação. Registre o resultado de qualquer limpeza aprovada na `.stat`.

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
