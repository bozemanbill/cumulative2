# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

An R Markdown analysis project. The main report is `analysis.Rmd`, which knits to `analysis.html`.

## Knitting / rendering

- **Knit via the RStudio "Knit" button only.** Do NOT render from the command line. Edit the `.Rmd`, then let the user knit in RStudio.
- Knitting requires `rmarkdown` and `knitr`, which are **not installed yet**.

## R environment

- Target version is **R 4.2.2**, installed at `C:\Program Files\R\R-4.2.2\`.
- **No R is on PATH** and ~10 versions are installed side by side, so a bare `Rscript`/`R` call won't resolve. Use the full version-specific path if a CLI invocation is ever truly needed.
- **No packages are installed.** Do not assume any package (tidyverse, etc.) is available, and do not run `install.packages(...)` without asking first.

## Git

- Local-only repo (no remote), default branch `main`.
- Commit only when the user explicitly asks. Work directly on `main`.
