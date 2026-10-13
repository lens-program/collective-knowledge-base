# LENS Collective Knowledge Base

One living document on **identifiability, recoverability, and related concepts**, maintained by
members of the [LENS Program](https://github.com/lens-program). It collects definitions from
different fields side by side, with citations and contributor names, along with connections
between concepts and open questions.

**Read it:** https://lens-program.github.io/collective-knowledge-base/

## Files

| File | What |
|---|---|
| [`terminology-and-references.qmd`](terminology-and-references.qmd) | The document. [Read it on the website](https://lens-program.github.io/collective-knowledge-base/) · [edit it on GitHub](https://github.com/lens-program/collective-knowledge-base/edit/main/terminology-and-references.qmd) |
| [`references.bib`](references.bib) | Shared bibliography (BibTeX); cite entries in the document as `[@key]` |
| `_quarto.yml` | Site settings |
| `.github/workflows/publish.yml` | Rebuilds and publishes the site when the document changes |

## How to contribute

Everything can be done in the browser. You do not need to install anything or know git.

### Add to the document

1. Open [`terminology-and-references.qmd`](terminology-and-references.qmd) and click the
   **pencil icon** (Edit this file), top right. Or use
   [this direct edit link](https://github.com/lens-program/collective-knowledge-base/edit/main/terminology-and-references.qmd).
2. Find the section you want. Each part and each concept starts with a banner like
   `PART: CONNECTIONS ACROSS FIELDS` or `CONCEPT: Identifiability`; use **Ctrl+F / Cmd+F** to jump to one.
3. Make your addition:
   - **A definition from your field:** add a new perspective block after the concept's last
     `### Perspective:` block. Copy the template in the comment under the
     `PART: TERMINOLOGY AND MATHEMATICAL DEFINITIONS` banner. Each perspective has three parts:
     **Definition** (in words), **Mathematical formulation** (in notation, with the assumptions
     it needs), and **References**. Do not rewrite another field's
     perspective. If you disagree with one, say so under `### Connections and distinctions`.
   - **An example or open question:** add a bullet under that concept's `### Examples` or
     `### Open questions`. Label it *(proposed)*, *(under discussion)*, or *(resolved)*.
   - **A new concept:** copy one whole concept, from its `CONCEPT:` banner down to the next
     banner, paste it after the last concept, and replace the text. Add a row for it to the
     *Terminology at a glance* table at the top. Give the heading a short
     id, e.g. `## Generic identifiability {#generic-identifiability}`.
   - **A connection between concepts:** add it under `### Connections and distinctions`, or
     to the table in `PART: CONNECTIONS ACROSS FIELDS`. Mark it *(proposed)* unless it is an
     established result.
4. Add a row with your name, the date, and what you added to the concept's
   `### Contributors` table. If you added a perspective, update its row in the
   *Terminology at a glance* table too.
5. Click **Commit changes…**, write a one-line description (e.g. "Add Bayesian definition of
   recoverability"), and commit. The website updates within a few minutes.

Math works as in LaTeX: `$\theta$` inline, `$$ ... $$` for displayed equations.

### Add a reference

1. Open [`references.bib`](references.bib) and click the **pencil icon**.
2. Paste the reference in BibTeX format. The easiest source is Google Scholar: click **Cite**
   under the paper, then **BibTeX**, and copy the entry.
3. Set the key (the first item after `@article{`) to `firstauthorYEARfirstword`, e.g.
   `rothenberg1971identification`. Keep entries in alphabetical order by key.
4. Commit the change.
5. Cite it in the document as `[@rothenberg1971identification]` for a parenthetical citation,
   or `@rothenberg1971identification` in running text. Cite several at once with
   `[@key1; @key2]`.

Every entry in `references.bib` appears in the References section at the end of the document,
whether or not it is cited yet.

### If something looks wrong

- **A citation shows as `?@key` on the website:** that key is not in `references.bib`, or is
  spelled differently there. Add or fix the entry.
- **The website did not update:** open the
  [Actions tab](https://github.com/lens-program/collective-knowledge-base/actions). A red ✗
  means the build failed. Click it to see the error, which usually points to the line to fix.
- GitHub's **Preview** tab while editing does not show citations or math, so do not worry if
  they look raw there.

To preview locally: `quarto preview` (requires [Quarto](https://quarto.org)).
