# HOSTING_DECISION_REQUIRED — Pacote para decisão humana de hospedagem

Estado: **decisão humana pendente**. Nada foi contratado, comprado,
configurado ou desligado. GitHub Pages permanece provisoriamente online.

Produto a hospedar: site estático multipágina (`index.html` +
`loja/` + `blog/` + `midias/` + `sobre/` + `contato/` + `assets/styles.css` +
`assets/favicon.svg` + `content/catalog.json` + `sitemap.xml` + `robots.txt`),
zero build, zero backend, zero analytics. Qualquer host estático serve;
saída a qualquer momento é copiar arquivos.

## Opção A (recomendada) — Cloudflare Pages

- Custo: plano gratuito US$ 0.
- Limites verificados na documentação oficial: 500 builds/mês por conta,
  100 domínios próprios por projeto, deploys de preview ilimitados, 1 build
  por vez no gratuito; projeto com builds frequentes usa fila.
  【2712500949425937882†L1-L7】
- Largura de banda: fontes secundárias convergem que o gratuito não mede
  transferência para conteúdo estático; confirmar na página oficial de preços
  no momento da decisão.
- Domínio próprio + HTTPS: incluídos no gratuito; DNS pode ficar onde já
  estiver, sem obrigação de mover tudo para a Cloudflare.
- Deploy: conecta o repositório Git e publica a cada push (ou upload manual).
- Lock-in: baixo — arquivos estáticos saem intactos; nada proprietário no
  produto.
- Carga operacional: mínima; sem servidor para manter.
- Privacidade: sem analytics embutido; nada muda no produto.

## Opção B — Netlify (alternativa)

- Custo: plano gratuito US$ 0, mas relatos secundários de 2025–2026 indicam
  mudança para modelo de créditos para contas novas (antes: 100 GB de banda
  e 300 min de build/mês); verificar os números vigentes na página oficial
  de preços antes de decidir.
- Domínio próprio + HTTPS: incluídos no gratuito.
- Deploy: Git-conectado ou arrastar-e-soltar manual; pré-visualizações por PR.
- Lock-in: baixo para site estático puro (evitar recursos proprietários
  como Forms/Functions para não criar acoplamento).
- Carga operacional: mínima.

## Opção C — Vercel Hobby (alternativa com ressalva)

- Custo: plano Hobby gratuito US$ 0.
- Limites verificados na documentação oficial: 100 GB de transferência
  Fast Data Transfer, 100 deploys/dia, 50 domínios por projeto, 2 CPUs de
  build, expiração de artefatos conforme tabela do plano.
  【3983849923775476849†L12-L35】
- Ressalva material: o Hobby é restrito a uso pessoal não comercial
  (fair use). Como o site prevê um dia oferecer algo (Prateleira), essa
  restrição pode colidir com o futuro — motivo para não ser a primeira opção.
  【3983849923775476849†L74-L78】
- Domínio próprio + HTTPS: incluídos.
- Lock-in: baixo para estático puro.
- Carga operacional: mínima.

## Descartadas nesta fase (com motivo)

- VPS/servidor próprio (qualquer provedor): custo mensal + manutenção,
  updates e hardening injustificáveis para um site estático de ~5 KB sem
  backend. Reavaliar somente se surgir necessidade material (backend, apps).
- Manter GitHub Pages como definitivo: rejeitado pela ADR-0002 — confunde
  versionamento com produção e prende a superfície canônica ao GitHub.

## Recomendação técnica

**Cloudflare Pages**: custo zero confirmado no essencial, limites oficiais
generosos para este porte, sem restrição de uso comercial no gratuito,
portabilidade total e operação mínima. Netlify como segunda opção; Vercel
Hobby apenas se o uso permanecer estritamente não comercial.

## O que a decisão humana precisa responder

1. Opção escolhida (A, B ou C).
2. Em qual conta/custódia adulta a conta do host será criada.
3. Quando comprar `matiasdecarvalho.com` (missão financeira separada) e onde
   ficará o DNS.
4. Autorização para a missão de publicação externa (deploy + validação +
   canonicalização), que só então poderá propor o desligamento do Pages.
