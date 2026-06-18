# Seamoon Pandey — Résumé

LaTeX source for my one-page résumé. AI & Backend Engineer.

- **Live links:** [GitHub](https://github.com/seamoonpandey) · [LinkedIn](https://www.linkedin.com/in/seamoonpandey/)
- **Output:** [`resume.pdf`](resume.pdf) (single page, A4)

## Build

Requires a LaTeX distribution with the `lato` font package (TeX Live full, or
`texlive-fontsextra`).

```bash
pdflatex -interaction=nonstopmode resume.tex
```

Output is written to `resume.pdf`. Run twice if cross-references ever change.

### Alternatives

- **Tectonic** (self-contained, fetches packages on demand):
  ```bash
  tectonic resume.tex
  ```
- **Overleaf:** upload `resume.tex` and compile with pdfLaTeX.

## Layout notes

- Single column throughout, for clean ATS (applicant-tracking-system) parsing.
- Sections: Summary, Technical Skills, Flagship Project, Selected Projects,
  Experience, Education.
- Tuned to fit one A4 page. If content is added, reclaim space via
  `\parskip`, the `\titlespacing` of `\section`, or the `geometry` margin
  (currently `0.6in`) before cutting content.
- Font: Lato 10pt. Section accent rules use `titlesec`.

## Files

| File | Purpose |
|------|---------|
| `resume.tex` | LaTeX source (edit this) |
| `resume.pdf` | Compiled output |
| `README.md` | This file |
| `.gitignore` | Ignores LaTeX build artifacts |
