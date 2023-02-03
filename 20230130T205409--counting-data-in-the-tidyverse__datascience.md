---
title: counting data in the tidyverse
date: 01-30-2023
tags: [datascience, tidyverse]
---

``` {R}
library(palmerpenguins)
library(dplyr)

penguins |>
  count(species, island)
```

  ----------- ----------- -------
  species     island      count
  Adelie      Biscoe      44
  Adelie      Dream       56
  Adelie      Torgersen   52
  Chinstrap   Dream       68
  Gentoo      Biscoe      124
  ----------- ----------- -------

# References

-   UT Austin DSC385
