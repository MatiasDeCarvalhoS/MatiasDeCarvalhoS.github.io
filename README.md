# Matias de Carvalho — Identidade digital independente

Site canônico provisório: `https://matiasdecarvalhos.github.io/`
Domínio futuro: `matiasdecarvalho.com` (sem compra nesta fase).
GitHub: `MatiasDeCarvalhoS/MatiasDeCarvalhoS.github.io` · SSH: `github-matias`.

## Princípios
Atenção antes de velocidade; processo visível; privacidade por padrão;
custódia adulta transparente; site como fonte canônica.

## Estrutura
- `index.html` — Home/hub (hero, loja, categorias, mídias, blog, institucional, CTA + rodapé)
- `loja/index.html` — Loja (catálogo, categorias, regras; estado vazio honesto)
- `blog/index.html` — Blog/Caderno (índice, estrutura de artigos, empty state)
- `midias/index.html` — Mídias (vídeos, projetos, links, galeria; sem contas inventadas)
- `sobre/index.html` — Sobre (terceira pessoa neutra, continuidade)
- `contato/index.html` — Contato (sem e-mail publicado, sem formulário falso, sem backend)
- `assets/styles.css` — linguagem “campo aberto” (tokens no próprio CSS)
- `assets/favicon.svg` — selo próprio (campo verde + semente palha)
- `content/catalog.json` — catálogo editorial (6 seções + campos futuros)
- `docs/HOSTING-DECISION.md` — pacote `HOSTING_DECISION_REQUIRED` (decisão humana pendente)
- `docs/IDENTITY.md` · `docs/ROADMAP.md` · `docs/PRIVACY-AND-SAFETY.md` · `docs/ARCHITECTURE.md` · `docs/adr/`
- `AGENTS.md` (regras de operação) · `PROJECT_STATE.md` (estado vigente; decisão material: ADR-0001)
- `.local/` — config operacional privada (gitignored, sem segredos)

## Operação
Autoria: operador adulto (repo-local). Remote `origin` via SSH exclusiva.
Sem analytics, sem tracking, sem checkout. Contato supervisionado.
