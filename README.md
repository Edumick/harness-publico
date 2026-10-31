# Harness Público — Marketplace de Plugins (Claude Code)

Marketplace **público** de plugins personalizados para o Claude Code, seguindo o padrão oficial de plugin marketplace. Reúne skills técnicas compartilháveis com a comunidade.

> Catálogo de skills técnicas compartilháveis, publicado como repositório público.

**Catálogo publicado:** https://edumick.github.io/harness-publico/

## Como instalar

Via [`npx skills`](https://github.com/vercel-labs/skills) (skills aninhadas em `plugins/*/skills/*` → `--full-depth`):

```bash
# Instalar todas as skills
npx skills add Edumick/harness-publico --full-depth

# Instalar as skills de um plugin
npx skills add Edumick/harness-publico/plugins/spec-driven-development/skills

# Instalar uma skill específica
npx skills add Edumick/harness-publico@brainstorm --full-depth
```

## Plugins

| Plugin | Descrição |
|--------|-----------|
| `spec-driven-development` | Fluxo spec-driven para software: escrever PRD e TRD |
| `uso-geral`                | Brainstorm e maturação de ideias antes de especificar ou implementar |

## Estrutura

```
harness-publico/
├── .claude-plugin/marketplace.json
├── plugins/<dominio>/
│   ├── .claude-plugin/plugin.json
│   ├── skills/<skill>/SKILL.md
│   └── docs/<skill>.md
└── site/               # vitrine local (Astro) — projeção pura do repositório
```

## Vitrine (site)

Publicada via GitHub Pages a cada push em `main` (workflow `.github/workflows/deploy-pages.yml`).

```bash
cd site
npm install
npm run dev        # http://localhost:4321
npm run build      # dist/ + busca Pagefind (npm run preview para ver a busca)
```

## Créditos

Este projeto é derivado do repositório original
[`fabricioveronez/harness-publico`](https://github.com/fabricioveronez/harness-publico),
criado por Fabrício Veronez. As skills e a estrutura original permanecem creditadas
ao autor. Verifique a licença do projeto original antes de redistribuir.

