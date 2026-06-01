# Linking Policy

- ligue documentos quando a relação ajudar a entender contrato, dependência, correlação ou continuidade;
- toda `.spec` deve apontar para sua `.stat` correspondente, e toda `.stat` deve apontar para sua `.spec` correspondente;
- quando houver um documento pai, um substituto ou uma referência relevante, linke também;
- use wikilinks ou links Markdown internos para notas `.md`;
- para arquivos que não são `.md` (`.json`, `.jsx`, `.py`, `.ts`, assets e similares), use referência explícita ao arquivo com o caminho exato ou texto literal; não use wikilink para criar nota nova a partir deles;
- não force links sem valor nem imponha limite numérico para correlações úteis;
- mantenha os links simples, estáveis e fáceis de seguir.

## Relacionados

- [../specs/README.md](../specs/README.md)
- [../specs/project.spec.md](../specs/project.spec.md)
- [../specs/project.stat.md](../specs/project.stat.md)
- [spec-stat.policy.md](spec-stat.policy.md)
