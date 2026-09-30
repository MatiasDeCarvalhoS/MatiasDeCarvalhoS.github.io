# Architecture — Matias de Carvalho

- Tipo: site estático, HTML + CSS, zero framework, zero build, zero analytics, zero cookies.
- Entrada: `index.html`; estilos: `assets/styles.css`; favicon: `assets/favicon.svg`.
- Catálogo editorial: `content/catalog.json`.
- Metadata: canonical `https://matiasdecarvalhos.github.io/`, Open Graph básico, `robots.txt`, `sitemap.xml`.
- Config operacional privada: `.local/` (gitignored) + mapa central `~/.config/familia-digital/account-map.json`.
- Remoto: `origin` → `git@github-matias:MatiasDeCarvalhoS/MatiasDeCarvalhoS.github.io.git` (SSH exclusiva).
- Hospedagem provisória: GitHub Pages do repo `<user>.github.io`; futura: domínio próprio.
- Isolamento: repo, remote, SSH, Chrome profile e Google próprios; nada compartilhado com irmãos.
