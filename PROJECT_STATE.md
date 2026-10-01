# Estado atual — Matias de Carvalho

Atualizado: 2026-10-01
Status: `SITE-PERSONALIZADO-CAMPO-ABERTO / HOSTING_DECISION_REQUIRED`

## Fatos vigentes

- Site “campo aberto” implementado e validado localmente (HTML+CSS, zero JS):
  Início, Projetos, Caderno, Sobre, Contato; selo próprio; estados vazios
  honestos; sem PII, analytics ou dependências externas.
- GitHub Pages (`https://matiasdecarvalhos.github.io/`) passa a SUPERFÍCIE
  PROVISÓRIA NÃO CANÔNICA (ver ADR-0002). GitHub = versionamento/backup.
  Produção futura = hospedagem independente, decisão humana pendente
  (`docs/HOSTING-DECISION.md` → `HOSTING_DECISION_REQUIRED`).
- Repo remoto `MatiasDeCarvalhoS/MatiasDeCarvalhoS.github.io` na Personal
  Account; chave SSH `matias-de-carvalho-github`; upstream `origin/main`.
- Identidade “campo aberto”, catálogo editorial e docs de identidade,
  arquitetura, roadmap e privacy/safety vigentes em `docs/`.
- SPEC ativa: `docs/SPEC-0001-digital-identity-foundation.md` (`PROPOSTA INICIAL`).
- Decisão material vigente: `docs/adr/ADR-0001-matias-owner-independente-referencia-metodologica-ilumino.md` — Matias é owner
  independente; iLúmino é referência metodológica, não parent workspace.
- Remote `origin` via SSH exclusiva `github-matias`, com upstream `origin/main`
  configurado no push inicial.

## Fronteiras vigentes

- Owner gravável único: `/home/andre/matias-de-carvalho`. Nada em
  `/home/andre/ilumino-workspace/repositories/`; nenhuma Organization, repo
  central familiar ou governança compartilhada.
- Zero dependência runtime/build do iLúmino; zero backlog, segredo, identidade
  ou conta compartilhados com Aurora, Tomás ou produtos iLúmino.
- Sem framework, backend, CMS, analytics ou domínio pago até necessidade
  comprovada (`economic-fit-first`).

## Próximo

- Decisão humana de hospedagem (`docs/HOSTING-DECISION.md`); depois, missão
  de publicação externa validada. Em paralelo, Fase 1 do `docs/ROADMAP.md`
  (primeiro projeto com passo a passo honesto).
