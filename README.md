# Ordinary Differential Equations

> ODE lecture notes and 30 weeks of fully worked homework, bilingual (Chinese/English), following 《常微分方程教程》 (A Course in Ordinary Differential Equations, 3rd ed.).

Unlike the other repositories in this series, the section headings here **keep the textbook's original numbering** (`## 1.1`, `## 6.2`, …), so the notes can be read directly against the book.

## Repository structure

```
ordinary-differential-equations/
├── cn/
│   ├── notes.md              # Chinese lecture notes (single file, 1095 lines)
│   └── homework/
│       └── week1.md … week30.md
├── en/
│   ├── notes.md              # Complete English translation (1095 lines, aligned)
│   └── homework/
│       └── week1.md … week30.md
└── textbooks/
    ├── ordinary-differential-equations.pdf   # Textbook scan (300 pp.)
    └── ordinary-differential-equations_ocr.pdf
```

## The notes

`notes.md` is a single file organized as **30 textbook-numbered sections**, including:

- 1.1 Differential equations and the definition of their solutions
- 2.1 Exact equations · 2.2 Separable equations · 2.3 First-order linear equations · 2.5 The integrating factor method
- 3.1 Picard's existence and uniqueness theorem · 3.2 Peano's existence theorem · 3.4 Comparison theorems
- 4.1 First-order implicit equations · 4.2 Singular solutions · 4.3 Envelopes
- 5.3 Continuous dependence on initial values and parameters
- 6.2 Linear systems with constant coefficients · 6.3 Higher-order linear equations
- 7.1 Cauchy's theorem · 7.2 Power series solutions · 7.3 Legendre polynomials
- 8.2 Stability of solutions · 8.3 Dynamical systems in the plane: singular points and limit cycles
- 10.x First integrals
- 11.1–11.3 First-order (quasi)linear PDEs

Every statement is a bold-tagged entry (**Definition**, **Theorem**, **Example**, **Algorithm**) with mathematics in `$…$` / `$$…$$`.

## The homework

Each `homework/weekN.md` follows the series-wide format:

1. **Toolbox** — a blockquote restating the definitions and theorems needed;
2. **Problems** — the assigned exercises;
3. **Solutions** — complete worked proofs ending with `$\blacksquare$`.

There are **30 weeks** of problem sets in each language.

## Bilingual layout

- `cn/` — authoritative Chinese version.
- `en/` — complete parallel English translation; files share identical names and line counts.

## The `textbooks/` folder

The two PDFs are the scanned textbook and its OCR copy — **external reference material**, not compiled from the notes. There is no build system; everything is plain Markdown rendered with GitHub's LaTeX support.

## Related repositories

Other course-notes repositories in the same series: [mathematical-analysis](https://github.com/wenje-ma/mathematical-analysis), [complex-analysis](https://github.com/wenje-ma/complex-analysis), [numerical-calculation-methods](https://github.com/wenje-ma/numerical-calculation-methods), and the full list on the [profile page](https://github.com/wenje-ma).
