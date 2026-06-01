# AGENTS.md

Este arquivo é voltado para agentes que vão aplicar a convenção em outro projeto.

Você está no repositório-fonte da convenção, não em um projeto alvo. Não confunda arquivos deste repositório com os arquivos que serão copiados para outro workspace. Ao aplicar a convenção, copie e adapte `templates/standard/` para o projeto destino. Não faça dogfood do repositório-fonte por conta própria sem pedido explícito.

O alias curto da convenção é `awc`, abreviação de `agent-workspace-convention`.

A versão e os metadados de controle da convenção vivem em `awc.meta.toon` na raiz do repositório.

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
- `agent/README.md`
- `docs/README.md`
- `docs/contracts/README.md`
- `docs/policies/README.md`
- `docs/reports/README.md`
- `docs/plans/README.md`
- `docs/guides/README.md`
- `docs/decisions/README.md`
- `docs/concepts/README.md`
- `docs/legacy/README.md`
- `.gitignore`
- `agent/policy/`
- `agent/specs/`
- `agent/tmp/.gitkeep`
- `agent/prints/.gitkeep`
- `agent/reports/.gitkeep`
- `agent/scripts/.gitkeep`
- `agent/test/.gitkeep`
- `agent/note/.gitkeep`

Quando o destino também for usado como vault do Obsidian, o template inclui o perfil recomendado de grafo em `templates/standard/.obsidian/graph.json`. Esse arquivo faz parte da implantação visual da convenção e pode ser copiado junto com o resto do template quando o vault aceitar a configuração padrão.

No perfil visual padrão da AWC, `README.md` e `AGENTS.md` devem ser tratados como nós de entrada privilegiados. Eles devem ficar em destaque no grafo para orientar a leitura inicial, porque normalmente aparecem espalhados por vários repositórios e funcionam como portas de entrada cognitivas da convenção.

Quando o vault for usado para inspeção técnica de implementação, pode ser útil copiar o perfil alternativo em `templates/standard/.obsidian/graph-tech.json`. Esse perfil é mais discreto e separa arquivos de código, configuração, testes e documentação sem substituir o perfil principal da convenção.

## Bootstrap seguro

Ao aplicar a convenção em um projeto alvo:

1. clone este repositório em uma pasta temporária fora do projeto alvo;
2. copie apenas o conteúdo de `templates/standard/`;
3. não copie a pasta `.git` deste repositório;
4. não mantenha o clone da convenção dentro do projeto alvo;
5. depois leia o `agent-start-here.md` criado no projeto alvo.

Se o projeto alvo já tiver `.gitignore`, mescle os padrões da convenção com os padrões existentes do projeto em vez de apagar regras úteis do repositório destino.

Exemplo:

```bash
tmp_dir="$(mktemp -d)"
git clone https://github.com/lucashahnndev/agent-workspace-convention.git "$tmp_dir/agent-workspace-convention"
cp -R "$tmp_dir/agent-workspace-convention/templates/standard/." .
```

## Grafo Obsidian recomendado

Quando o projeto alvo usar Obsidian como vault, aplique o perfil padrão em
`templates/standard/.obsidian/graph.json` e mantenha como ruído excluído:

- `changelog` e `CHANGELOG`
- dependências e artefatos de build como `node_modules`, `vendor`, `dist` e `build`
- ambientes locais como `.venv`, `venv` e `site-packages`
- arquivos e pastas de configuração do próprio vault como `.git` e `.obsidian`

Se a localização dessas pastas variar, configure também **Excluded files** no
Obsidian, porque essa opção oculta os arquivos na Search, Graph View e backlinks
de forma global no vault.

## Pós-bootstrap: adequação inicial

Depois de aplicar `templates/standard/`, leia o `agent-start-here.md` criado e rode `git status --short`. Se houver arquivos modificados, untracked ou bagunça operacional, faça um diagnóstico e classifique cada item em manter, investigar, mover, renomear, apagar ou preservar. Não apague, mova, faça `reset`, `stash` ou commit sem aprovação. Registre o resultado de qualquer adequação aprovada na `.stat`.

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

## Protocolo de adequação

Quando a convenção for aplicada em um projeto alvo, o fluxo recomendado é:

1. bootstrap da convenção;
2. ajustar `graph.json` e `.gitignore` para ruído local conhecido;
3. inventariar artefatos, arquivos soltos e temporários;
4. pedir aprovação antes de organizar ou apagar;
5. organizar o repositório;
6. mapear documentação que precisa virar contexto, `.spec` ou `.stat`;
7. pedir aprovação antes de criar ou mover contratos;
8. fazer a linkagem e a consolidação;
9. atualizar `.stat` com o progresso real;
10. usar `trace_id` para registrar a mudança relevante.

Se faltar contexto para a próxima ação, siga [templates/standard/agent/policy/adequation.policy.md](templates/standard/agent/policy/adequation.policy.md).
Depois do bootstrap, use a mensagem padrao de handoff da adequacao e peça aprovacao antes de entrar na fase seguinte.
