# cumulative

An R Markdown analysis project.

## Requirements

- R 4.2.2
- RStudio
- (Packages will be added as the analysis develops.)

## Project structure

```
cumulative/
├── cumulative.Rproj   # RStudio project file — open this to start
├── analysis.Rmd       # Main analysis; knits to analysis.html
├── README.md          # This file
└── .gitignore         # R-oriented ignore rules
```

## Getting started

1. Open `cumulative.Rproj` in RStudio (this sets the working directory to the
   project root and isolates the session).
2. Open `analysis.Rmd`.
3. Click **Knit** (or run `rmarkdown::render("analysis.Rmd")`) to produce
   `analysis.html`.

## Rendering from the console

```r
rmarkdown::render("analysis.Rmd")
```

> Note: knitting requires the `rmarkdown` and `knitr` packages. Install them
> when you're ready with `install.packages(c("rmarkdown", "knitr"))`.
