# LENS Knowledge Base

A living, cross-disciplinary reference on **identifiability, recoverability, and related
concepts**, maintained by members of the [LENS Program](https://github.com/lens-program).

**Site:** https://lens-program.github.io/collective-knowledge-base/

Each concept page collects definitions from different fields side by side, with citations and
contributor attribution. Seminar notes link back to the concepts they touch, and unresolved
questions go into a shared Open Problems list.

## Layout

| Path | What |
|---|---|
| `concepts/` | One `.qmd` per concept; `_template.qmd` is the entry template |
| `seminars/` | Notes from LENS talks; `_template.qmd` is the notes template |
| `connections.qmd` | Relationships among concepts and cross-field equivalences |
| `open-problems.qmd` | Open questions |
| `references.bib` | Shared bibliography (BibTeX) |
| `CONTRIBUTING.md` | How to contribute (also rendered on the site) |
| `.github/workflows/publish.yml` | Renders with Quarto and deploys to GitHub Pages on push to `main` |

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). The short version: add a definition next to the
existing ones instead of overwriting them, cite it, and sign it.

## Building locally

Requires [Quarto](https://quarto.org/docs/get-started/).

```bash
quarto preview
```
