# Architecture — Matias de Carvalho

- Tipo: site estático, HTML + CSS, zero framework, zero build, zero analytics, zero cookies.
- Entrada: `index.html`; estilos: `assets/styles.css`; favicon: `assets/favicon.svg`.
- Catálogo editorial: `content/catalog.json`.
- Metadata: canonical `https://matiasdecarvalhos.github.io/`, Open Graph básico, `robots.txt`, `sitemap.xml`.
- Config operacional privada: `.local/` (gitignored, repo-local; sem segredos).
- Remoto: `origin` → `git@github-matias:MatiasDeCarvalhoS/MatiasDeCarvalhoS.github.io.git` (SSH exclusiva).
- Hospedagem provisória: GitHub Pages do repo `<user>.github.io`; futura: domínio próprio.
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
