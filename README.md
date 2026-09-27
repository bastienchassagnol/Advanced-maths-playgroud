# Advanced maths playground

Quarto **website** (HTML only) for visual notes: differential
equations, linear algebra, analysis, and probability. The folder
layout follows
[Rag-llm-playground](https://github.com/bastienchassagnol/Rag-llm-playground);
the project type is a
[website](https://quarto.org/docs/websites/#config-file), not a book.

## Contents

| Page | Path |
|------|------|
| Welcome | `index.qmd` |
| Differential equations | `dynamics/differential-equations.qmd` |
| Linear algebra | `linear-algebra/matrix-decompositions.qmd` |
| Analysis | `analysis/calculus-and-complex.qmd` |
| Statistics and probability | `statistics/probability.qmd` |

Instagram stills (from [@eeanimation](https://www.instagram.com/eeanimation/))
are lightbox galleries. Re-fetch with `/instagram-carousel`.

## Build

```bash
quarto preview         # live HTML
quarto render          # writes HTML under docs/
```

Quarto ≥ 1.8. Computations use freeze (`execute.freeze: auto`) if you
later enable evaluation. There is no PDF format.

## GitHub Pages

Publishing follows the
[Quarto publish Action](https://quarto.org/docs/publishing/github-pages.html#publish-action).

1. Once, from a machine that can push: `quarto publish gh-pages`
   (creates the `gh-pages` branch; GitHub Pages publishes are *not*
   stored in `_publish.yml`).
2. Workflow: [`.github/workflows/publish.yml`](.github/workflows/publish.yml)
   — official [publish Action](https://quarto.org/docs/publishing/github-pages.html#publish-action),
   on push to `main` and on **workflow_dispatch**.
3. In the GitHub repo: **Settings → Actions → General → Workflow
   permissions → Read and write**. **Settings → Pages** should
   deploy from the `gh-pages` branch.

Site URL:
<https://bastienchassagnol.github.io/Advanced-maths-playgroud/>.

## Attribution

- Site structure after [Rag-llm-playground](https://github.com/bastienchassagnol/Rag-llm-playground).
- Galleries: EE Animations Instagram carousels (see each page).
