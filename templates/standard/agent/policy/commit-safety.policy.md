# Commit Safety Policy

- rode `git status --short` antes de propor ou fazer commit;
- revise o diff;
- se o projeto usa Git, mudanças relevantes devem terminar com `.stat` atualizada; quando aprovado, devem terminar também com commit limpo e coerente;
- use um `trace_id` curto e estável para amarrar a mudança antes do commit;
- formato recomendado do `trace_id`: `awc-YYYYMMDD-HHMM-xxxx`, em UTC, com `xxxx` alfanumérico curto;
- registre o `trace_id` na `.stat` e também no commit message ou no corpo do commit;
- a `.stat` pode registrar o hash depois do commit, mas não depende dele para existir;
- se o commit não for feito, a `.stat` deve registrar o motivo e o estado de rastreio;
- não misture no commit arquivos fora do escopo da etapa;
- não commite segredos, `.env`, dumps, snapshots ou logs sensíveis;
- não commite temporários por acidente;
- prefira commits pequenos por etapa;
- se necessário, separe mudança de contrato, implementação e limpeza.
