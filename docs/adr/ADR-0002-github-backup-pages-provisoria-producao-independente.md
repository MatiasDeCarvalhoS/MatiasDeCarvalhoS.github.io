# ADR-0002 — GitHub como versionamento/backup; Pages como superfície provisória; produção futura em hospedagem independente

- Data: 2026-10-01
- Estado: aceita
- Escopo: `matias-de-carvalho` (owner `/home/andre/matias-de-carvalho`)
- Complementa: ADR-0001 (owner independente; iLúmino como referência metodológica)

## Contexto

O site de Matias de Carvalho foi publicado inicialmente via GitHub Pages
(`https://matiasdecarvalhos.github.io/`), a partir do repositório
`MatiasDeCarvalhoS/MatiasDeCarvalhoS.github.io`. Essa publicação cumpriu a
função de fundação (Fase 0), mas confunde dois papéis distintos: o GitHub
como controle de versão e o GitHub como superfície de produção. A arquitetura
desejada separa esses papéis.

## Decisão

- `GitHub = SOURCE_CONTROL_AND_BACKUP` — versionamento e backup remoto.
  Permitidos: commit, push, fetch, verificação de ancestry. Não é host de
  produção.
- `GitHub Pages = SUPERFÍCIE PROVISÓRIA NÃO CANÔNICA` — permanece online
  somente para evitar despublicação prematura. Não representa o produto final.
- `Produção futura = HOSPEDAGEM INDEPENDENTE` — site estático portátil
  (HTML+CSS, zero build), publicável em qualquer host estático, sob decisão
  humana explícita (ver `docs/HOSTING-DECISION.md`).
- `matiasdecarvalho.com = DOMÍNIO CANÔNICO FUTURO` — ainda não adquirido;
  aquisição, DNS e canonicalização em missão financeira/operacional separada,
  após aprovação humana da hospedagem e validação da publicação externa.
- Desligamento do GitHub Pages SOMENTE após: hospedagem aprovada, site
  publicado nela, produção externa validada, domínio/canonicalização
  decididos, e missão específica autorizando a retirada.

## Consequências

- `docs/ARCHITECTURE.md`, `README.md` e `PROJECT_STATE.md` declaram os papéis
  acima; nenhuma automação de deploy via GitHub Actions nesta missão.
- O produto permanece estático e portátil para manter o custo de troca
  próximo de zero (`economic-fit-first`).
- Nenhuma conta, contratação, compra de domínio, mudança de DNS ou
  desligamento do Pages nesta missão.
