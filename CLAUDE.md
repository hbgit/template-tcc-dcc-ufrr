# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

LaTeX templates for final-year projects (TCC) at DCC/UFRR (Departamento de Ciência da Computação, Universidade Federal de Roraima), plus a PPCA (graduate program) qualification template. All content, comments and commit messages are in Brazilian Portuguese. The templates follow Resolução CEPE/UFRR nº 133/2025 (Seção 3.1 for monografia, Seção 3.2 for artigo) with DCC-specific adaptations. There is no code, test suite or CI — only LaTeX.

## Building

Each template in `modelos/` is a self-contained LaTeX project; compile from inside its directory (paths like `estilo/sbc-template` and `capas/capa` are relative). Bibliography uses BibTeX via `abntex2cite` (`\usepackage[alf]{abntex2cite}`), so a full build is:

```bash
cd modelos/Bacharelado-Comp/TCC_2_artigo
pdflatex tcc-2-main && bibtex tcc-2-main && pdflatex tcc-2-main && pdflatex tcc-2-main
# or: latexmk -pdf tcc-2-main.tex
```

Main files per template:
- `modelos/Bacharelado-Comp/TCC_1_artigo/tcc-1-main.tex`
- `modelos/Bacharelado-Comp/TCC_2_artigo/tcc-2-main.tex`
- `modelos/Bacharelado-Comp/TCC_1_monografia/dcc-modelo-tcc1.tex`
- `modelos/PPCA/qualificacao/qualificacao-main.tex`

Build artifacts (`*.aux *.bbl *.blg *.log *.toc`) are gitignored; the committed `.pdf` in each template is the rendered example and is updated alongside template changes.

## Architecture

Two independent template families:

**Artigo family** (`TCC_1_artigo`, `TCC_2_artigo`, `PPCA/qualificacao`) — `article` class + the SBC article style in `estilo/sbc-template.sty` (with `sbc.bst`, `caption2.sty`). Layout per template:
- Main `.tex` sets metadata with custom macros defined in `sbc-template.sty`: `\title`, `\author`, `\orientador`, `\coorientador`, `\address`, `\agradecimento`, `\keywords`. Empty `\coorientador{}` / `\agradecimento{}` hide those parts via `\ifcoorientadordefined` / `\ifagradecimentodefined`.
- `capas/` — cover, title page, acknowledgements, annex cover; these read the metadata macros and are not meant to be edited by students.
- `secoes/` — one file per article section (`\input`), plus annexes (`\include`). TCC 2 and PPCA additionally have `ficha_catalografica.tex` and `ata-aprovacao.tex` (filled after the defense).
- TCC 1 has `sec-plan-experimentos` (planning) and an appendix; TCC 2 replaces it with `sec-ava-experimentos` (evaluation).

**Monografia family** (`TCC_1_monografia`) — uses a vendored abnTeX2 class (`abntex2/abntex2.cls`, `abntex2cite.sty`, `abntex2abrev.sty`, DCC logo) and a `memoir`-style chapter structure in `capitulos/NN_*.tex`. Pre-textual elements (capa, folha de rosto, resumo, etc.) live directly in `dcc-modelo-tcc1.tex`.

**Duplication is intentional:** each template carries its own copy of `estilo/` (or `abntex2/`) so students can download a single folder. `PPCA/qualificacao` was forked from `TCC_2_artigo` (identical main file and `estilo/` except `logo-ppca.png`; `capas/` differ). A fix to `sbc-template.sty` or a shared `capas/` file usually needs to be applied to every artigo template — check with `diff -r` between template dirs. Note the PPCA and TCC 2 READMEs are copies and still reference `tcc-1-main.tex`.

## Contributing conventions

From `CONTRIBUTING.md` / `pull_request_template.md`: keep the modular structure (style in `.sty`, content in `secoes/`/`capitulos/`), follow existing naming, and use descriptive branch names and Portuguese commit messages. Work happens on `develop`; PRs target `main`.
