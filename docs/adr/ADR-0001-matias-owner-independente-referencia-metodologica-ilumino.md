# ADR-0001 — Matias como owner independente; iLúmino como referência metodológica

- Data: 2026-09-30
- Estado: aceita
- Escopo: `matias-de-carvalho` (owner `/home/andre/matias-de-carvalho`)

## Contexto

O projeto de Matias de Carvalho adota localmente a maturidade
documental/metodológica desenvolvida no `ilumino-workspace` (documentação viva,
`AGENTS.md`, `PROJECT_STATE.md`, SPEC/ADR, owner e `write_scope` explícitos,
separação fato/hipótese/decisão, gates `PREWRITE`/`PRECOMMIT`/`PREPUSH`/`CLOSEOUT`,
validação por evidência, preservação de ancestry Git, política de segredos,
`economic-fit-first`, mudanças pequenas e reversíveis). Era preciso formalizar
se essa adoção implica vínculo arquitetural — ou seja, se Matias deveria residir
fisicamente no workspace iLúmino.

## Decisão

- `matias-de-carvalho` é um owner independente, com workspace próprio em
  `/home/andre/matias-de-carvalho` e GitHub Personal Account própria
  (`MatiasDeCarvalhoS`, repo `MatiasDeCarvalhoS/MatiasDeCarvalhoS.github.io`).
- `ilumino-workspace` é referência exclusivamente metodológica: organiza o
  projeto, não o contém. Não é parent workspace arquitetural.
- Nenhuma dependência de runtime/build do `ilumino-workspace`; nenhum symlink
  para governança; nenhuma propriedade Git compartilhada; nenhum backlog,
  segredo ou identidade compartilhados; nenhuma sincronização automática.
- Não criar Organization, repositório central familiar, quarto projeto de
  governança ou dependência compartilhada com Aurora/Tomás.

## Alternativa rejeitada

Colocar o projeto de Matias em `/home/andre/ilumino-workspace/repositories/`.
Rejeitada porque residência física no workspace iLúmino sugeriria pertencimento
arquitetural ao ecossistema iLúmino, criaria acoplamento de ownership
(write_scope compartilhado, governança cruzada) e violaria a independência de
contas, identidade e custódia exigida para o projeto de uma criança.

## Consequências

- `docs/ARCHITECTURE.md` declara a independência física, de ownership e de
  runtime/build; `AGENTS.md` fixa owner e `write_scope`; `PROJECT_STATE.md`
  registra este ADR como decisão material vigente.
- Missões futuras mantêm leitura do iLúmino como read-only metodológico,
  sem copiar governança específica dos produtos iLúmino.
