# Workspace Policy

- `agent/` é workspace operacional;
- `tmp` guarda temporários;
- `prints` guarda capturas e imagens de teste;
- `reports` guarda relatórios e evidências textuais;
- `scripts` guarda scripts auxiliares;
- `test` guarda testes pontuais;
- `note` guarda anotações internas;
- `agent/.gitignore` ignora conteúdo operacional temporário por padrão; `agent/specs/`, `agent/policy/`, `agent/scripts/` e `agent/test/` continuam versionáveis; se algo em `tmp`, `prints`, `reports` ou `note` virar evidência durável, promova para o local correto antes de versionar.
- workspace não é documentação oficial;
- nada ali vira contrato por acidente;
- temporários devem ser limpos ou promovidos;
- não espalhe arquivos fora do workspace.
