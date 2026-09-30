# AGENTS.md — Matias de Carvalho

## Owner e escopo de escrita

- Owner gravável único: `/home/andre/matias-de-carvalho`.
- `write_scope = ["/home/andre/matias-de-carvalho"]`.
- Não escrever em `/home/andre/ilumino-workspace`; leitura lá é SOMENTE leitura
  (princípios/metodologia) e nunca concede escrita nem cria vínculo.
- Não escrever nem inspecionar desnecessariamente projetos de Aurora ou Tomás.
- Não alterar contas, credenciais, SSH, Chrome, remoto GitHub, Pages ou
  infraestrutura sem instrução explícita.

## Identidade do projeto

- Nome público: `Matias de Carvalho`. Workspace canônico: `/home/andre/matias-de-carvalho`.
- GitHub Personal Account: `MatiasDeCarvalhoS`; repo alvo:
  `MatiasDeCarvalhoS/MatiasDeCarvalhoS.github.io`.
- Matias NÃO pertence arquiteturalmente ao ecossistema iLúmino. `ilumino-workspace`
  é referência metodológica, não parent workspace (ver ADR-0001).

## Ordem de leitura

1. Este `AGENTS.md`;
2. `PROJECT_STATE.md`;
3. A SPEC ou ADR ativa nele referenciada;
4. `docs/` (`IDENTITY.md`, `ARCHITECTURE.md`, `ROADMAP.md`, `PRIVACY-AND-SAFETY.md`);
5. Git, diff e validações conforme a necessidade.

## Regras de operação

1. Mudança material registra antes uma SPEC curta ou ADR com objetivo, limites e
   validação proporcional. Decisões materiais vão para `docs/adr/`.
2. Separar fato observado de hipótese e de decisão, em docs e em relatos.
3. Gates: `PREWRITE` (branch, HEAD, status, remote/upstream, ancestry),
   `PRECOMMIT` (revisão integral do diff), `PREPUSH` e `CLOSEOUT`
   (veredito factual, HEAD inicial/final, arquivos, validações, pendências).
4. Validar por evidência: executar quando razoável; nunca fabricar PASS.
   Proporcional ao estágio — site estático sem build exige no mínimo revisão
   integral do diff e checagem de consistência entre documentos.
5. Preservar ancestry Git: sem `reset --hard`, rebase destrutivo, force-push,
   `filter-branch`/`filter-repo` ou alteração de remote sem autorização material.
6. Segredos e PII operacional (credenciais, emails, telefones, escola, endereço,
   rotina, documentos) nunca entram em docs, logs, prompts ou Git. `.local/` é
   gitignored e repo-local; nada compartilhado com Aurora, Tomás ou iLúmino.
7. `economic-fit-first`: decisões futuras de stack/superfície (framework, backend,
   CMS, analytics, domínio pago) exigem necessidade comprovada e missão separada.
8. Mudanças pequenas, verificáveis e reversíveis. Não introduzir framework,
   backend, CMS, analytics ou infraestrutura nova sem decisão explícita.
9. Não sofisticar artificialmente a identidade pública de uma criança: a
   metodologia organiza o projeto; autoridade só se declara com realização
   verificável.
