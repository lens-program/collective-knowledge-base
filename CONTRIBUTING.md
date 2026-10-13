## Ground rules

1. **Add, don't overwrite.** If your field defines a concept differently, add a new
   subsection under "Definitions across fields". If you disagree with an existing definition,
   say so under "Connections and distinctions", or open an issue.
2. **Cite formal definitions.** Every definition gets at least one `@key` citation to an
   entry in `references.bib`.
3. **Sign your contribution.** Add a row to the page's Contributors table, and put a
   `*Contributed by:* Name (date)` line under any new definition.
4. **Label interpretation.** Mark proposed connections *(proposed)* and unresolved questions
   *(open)*. Do not present them as established results.
5. **No implied consensus.** A page states a LENS position only after the group has discussed
   and agreed on it, and then it says so explicitly.

## Ways to contribute, easiest first

### 1. Open an issue (no Git needed)

Use the [issue forms](https://github.com/lens-program/collective-knowledge-base/issues/new/choose)
to propose a term, suggest a reference, or raise an open question. A maintainer will fold it in.

### 2. Edit in the browser

Every page on the site has an **Edit this page** link. It opens the file in GitHub's web
editor. Make your change, then choose **Propose changes**: GitHub creates a branch and a pull
request for you.

### 3. Work locally

```bash
git clone https://github.com/lens-program/collective-knowledge-base.git
cd collective-knowledge-base
git checkout -b add-<topic>
quarto preview          # live preview at http://localhost:4200
```

Commit, push your branch, and open a pull request.

## Adding a concept

Copy `concepts/_template.qmd` to `concepts/<concept-name>.qmd` (lowercase, hyphens). Fill in
what you know and leave the rest short. Add the page to the sidebar in `_quarto.yml`.

## Adding a reference

Add a BibTeX entry to `references.bib`:

- key format `firstauthorYEARfirstword`, e.g. `rothenberg1971identification`;
- keep entries in alphabetical order by key, so simultaneous additions merge cleanly;
- include a `doi` field only once you have checked it against the publisher page.

Cite it on any page with `@key` (in text) or `[@key]` (in parentheses). It then appears on the
References page automatically.

## Adding seminar notes

Copy `seminars/_template.qmd` to `seminars/YYYY-MM-DD-speaker.qmd`. Tag it with the concepts
it touches, and copy any new questions to `open-problems.qmd`.

## Review and publishing

Pull requests to `main` need one approving review. Reviewers check that citations resolve, the
site renders, and existing definitions were added to rather than overwritten. Once a pull
request is merged, GitHub Actions rebuilds and publishes the site within a few minutes.
