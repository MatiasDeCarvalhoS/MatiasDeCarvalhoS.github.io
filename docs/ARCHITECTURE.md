# Architecture — Matias de Carvalho

- Tipo: site estático, HTML + CSS, zero framework, zero build, zero analytics, zero cookies.
- Tipo: site estático multipágina, HTML + CSS, zero framework, zero build, zero JS, zero analytics, zero cookies.
- Entradas: `index.html` (Home/hub) + `loja/`, `blog/`, `midias/`, `sobre/`, `contato/` (cada uma com `index.html` próprio); estilos: `assets/styles.css`; favicon: `assets/favicon.svg` (selo próprio: campo verde + semente palha). Paths relativos — funciona em qualquer servidor HTTP estático, em qualquer base.
- Linguagem visual: “campo aberto” — base branca, verde `#14532d`, acento palha `#d9a521`, divisórias finas, seções numeradas, hero panorâmico em composição gráfica abstrata própria (sem fotografia de pessoa), tokens simples no próprio CSS.
- Arquitetura da informação: Início (hub), Loja, Blog/Caderno, Mídias, Sobre, Contato (+ rodapé verde-escuro com navegação). Sem páginas vazias artificiais; estados vazios honestos. Sem carrinho, checkout, login, comentários, API, banco ou formulário funcional.
- Catálogo editorial: `content/catalog.json` (espelha as 6 seções + campos futuros de produto/post, sem itens fictícios).
- Metadata: title/description por página, Open Graph básico sem `og:url`; sem tag `canonical` (não há domínio canônico real; `github.io` não é declarado canônico final). `robots.txt`, `sitemap.xml` (6 URLs da superfície provisória).
- Config operacional privada: `.local/` (gitignored, repo-local; sem segredos).
- Remoto: `origin` → `git@github-matias:MatiasDeCarvalhoS/MatiasDeCarvalhoS.github.io.git` (SSH exclusiva).

## Papéis de hospedagem (ver ADR-0002)

- GitHub = `SOURCE_CONTROL_AND_BACKUP` (versionamento/backup; não é produção).
- GitHub Pages = superfície provisória não canônica (online para evitar despublicação prematura; desligamento só em missão própria futura).
- Produção futura = hospedagem independente (decisão humana pendente — ver `docs/HOSTING-DECISION.md`).
- Domínio canônico futuro: `matiasdecarvalho.com` (não adquirido).

- Isolamento: repo, remote, SSH, Chrome profile e Google próprios; nada compartilhado com irmãos.

## Independência de ownership e física (ver ADR-0001)

- Owner gravável único: `/home/andre/matias-de-carvalho`. Este projeto NÃO reside em
  `/home/andre/ilumino-workspace/repositories/` e não deve ser movido para lá
  (alternativa rejeitada em ADR-0001).
- Conta GitHub própria (Personal Account): `MatiasDeCarvalhoS`; repositório alvo:
  `MatiasDeCarvalhoS/MatiasDeCarvalhoS.github.io`. Nenhuma Organization, repositório
  central familiar, quarto projeto de governança ou propriedade Git compartilhada.
- `ilumino-workspace` é referência exclusivamente metodológica (documentação viva,
  `AGENTS.md`, `PROJECT_STATE.md`, SPEC/ADR, gates, validação por evidência). Não é
  parent workspace arquitetural de Matias.
- Zero dependência de runtime/build de `ilumino-workspace`: nenhum symlink para
  governança, nenhum import/build/runtime cruzado, nenhuma sincronização automática.
- Zero compartilhamento operacional: nenhum backlog, segredo, identidade, credencial
  ou conta compartilhados com Aurora, Tomás ou qualquer produto iLúmino. Leitura
  eventual do workspace iLúmino é somente leitura e não concede escrita nem cria vínculo.
