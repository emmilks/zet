---
title: counting data in the tidyverse
date: 01-30-2023
tags: [datascience, tidyverse]
---

``` {r}
library(palmerpenguins)
library(dplyr)

penguins |>
  select(species, island, flipper_length_mm) |>
  mutate(flipper_length_cm = flipper_length_mm / 10,
         flipper_length_in = flipper_length_mm / 25.4) |>
  head()
```

  --------- ----------- -------------------------------- -------------------------------- --------------------------------
  species   island      `flipper_length_mm`   `flipper_length_cm`   `flipper_length_in`
  Adelie    Torgersen   181                              18.1                             7.1259842519685
  Adelie    Torgersen   186                              18.6                             7.32283464566929
  Adelie    Torgersen   195                              19.5                             7.67716535433071
  Adelie    Torgersen
  Adelie    Torgersen   193                              19.3                             7.59842519685039
  Adelie    Torgersen   190                              19                               7.48031496062992
  --------- ----------- -------------------------------- -------------------------------- --------------------------------

# References

-   UT Austin DSC385
