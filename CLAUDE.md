# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

An R Markdown analysis project that analyzes spatial **shapefiles of wetlands**. The main report is `analysis.Rmd`, which knits to `analysis.html`.

Reading shapefiles needs a spatial package (e.g. `sf`), which is **not installed** — don't assume it's there; ask before installing (see R environment below).

## Working style

The author is an **advanced-novice R user**. When writing or changing code here:
- Explain the reasoning as you go — don't just hand over code.
- Prefer **readable code over clever code**.
- Use the **tidyverse where it genuinely helps**; plain base R is fine when it's clearer.

## Knitting / rendering

- **Knit via the RStudio "Knit" button only.** Do NOT render from the command line — RStudio bundles pandoc and sets it up on Knit, but it is not on PATH, so a CLI render fails with "pandoc not available". Edit the `.Rmd`, then let the user knit in RStudio.
- `rmarkdown` (2.31) and `knitr` (1.45) are installed in the R 4.2.2 user library (`%LOCALAPPDATA%\R\win-library\4.2`).

## R environment

- Target version is **R 4.2.2**, installed at `C:\Program Files\R\R-4.2.2\`.
- **No R is on PATH** and ~10 versions are installed side by side, so a bare `Rscript`/`R` call won't resolve. Use the full version-specific path if a CLI invocation is ever truly needed.
- Only `rmarkdown` + `knitr` (and their deps) are installed. Do not assume other packages (tidyverse, etc.) are available, and do not run `install.packages(...)` without asking first.

## Git

- Remote `origin` → https://github.com/bozemanbill/cumulative2, default branch `main`.
- Commit only when the user explicitly asks. Work directly on `main`.
