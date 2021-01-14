
<!-- README.md is generated from README.Rmd. Please edit that file -->

# equatags

<!-- badges: start -->

[![R build
status](https://github.com/davidgohel/equatags/workflows/R-CMD-check/badge.svg)](https://github.com/davidgohel/equatags/actions)
[![Lifecycle:
maturing](https://img.shields.io/badge/lifecycle-maturing-blue.svg)](https://www.tidyverse.org/lifecycle/#maturing)
<!-- badges: end -->

The goal of the package is to provide a tool to transform equations
expressed in `latex`, `MathML` or `ASCIIMathML` into `SVG` format
(i.e. as an image) and `Office Open XML Math` format (which can be used
in a Word or PowerPoint document).

## Installation

You can install the development version from GitHub with:

``` r
# install.packages("devtools")
devtools::install_github("davidgohel/equatags")
```

## Example

``` r
library(equatags)
x <- c("(ax^2 + bx + c = 0)",
       "x = {-b \\pm \\sqrt{b^2-4ac} \\over 2a}")
z <- transform_mathjax(x = x, to = "svg")

writeLines(z[1], "man/figures/eq1.svg", useBytes = TRUE)
writeLines(z[2], "man/figures/eq2.svg", useBytes = TRUE)
```

![equation 1](man/figures/eq1.svg) ![equation 2](man/figures/eq2.svg)
