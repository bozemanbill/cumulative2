---
name: new-analysis
description: Scaffold a new R Markdown report from the project template. Use when the user wants to start a new analysis/report file, e.g. "/new-analysis sales-q3".
disable-model-invocation: true
---

Create a new R Markdown report named from `$ARGUMENTS` (the report's base name; e.g. `sales-q3` → `sales-q3.Rmd`). If `$ARGUMENTS` is empty, ask the user for a name.

Steps:
1. Slugify the name (lowercase, spaces/underscores → hyphens, strip extension if the user typed `.Rmd`). The file is `<slug>.Rmd` at the project root.
2. If `<slug>.Rmd` already exists, stop and tell the user — do not overwrite.
3. Write `<slug>.Rmd` reusing the YAML header and structure of `analysis.Rmd`:
   - Same `output: html_document` block (toc, toc_float, number_sections, code_folding, theme cosmo, df_print paged).
   - Set `title` to a Title-Cased version of the name.
   - Keep the `setup` chunk with the same `knitr::opts_chunk$set(...)` options.
   - Keep the section skeleton (Overview → Setup → Data → Exploration → Analysis → Results → Session info) with the same commented-out hints.
4. Do NOT knit it (this project knits via the RStudio Knit button only — see CLAUDE.md).
5. Tell the user the file was created and that they can open and Knit it in RStudio.
