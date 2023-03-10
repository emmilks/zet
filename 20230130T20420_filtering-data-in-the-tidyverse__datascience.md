---
title: filtering data in the tidyverse
date: 01-30-2023
tags: [datascience, tidyverse]
---

``` {R}
library(palmerpenguins)
library(dplyr)

penguins |>
  filter(species == "Gentoo") |>
  head()
```

  --------- -------- ----------------------------- ---------------------------- -------------------------------- ------------------------------ -------- ------
  species   island   `bill_length_mm`   `bill_depth_mm`   `flipper_length_mm`   `body_mass_grams`   sex      year
  Gentoo    Biscoe   46.1                          13.2                         211                              4500                           female   2007
  Gentoo    Biscoe   50                            16.3                         230                              5700                           male     2007
  Gentoo    Biscoe   48.7                          14.1                         210                              4450                           female   2007
  Gentoo    Biscoe   50                            15.2                         218                              5700                           male     2007
  Gentoo    Biscoe   47.6                          14.5                         215                              5400                           male     2007
  Gentoo    Biscoe   46.5                          13.5                         210                              4550                           female   2007
  --------- -------- ----------------------------- ---------------------------- -------------------------------- ------------------------------ -------- ------

# References

-   UT Austin DSC385
