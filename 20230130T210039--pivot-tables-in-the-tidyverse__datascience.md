---
title: pivot tables in the tidyverse
date: 01-30-2023
tags: [datascience, tidyverse]
---

``` {r}
library(palmerpenguins)
library(dplyr)

penguins |>
  group_by(species, island) |>
  summarize(
    n = n(),
    mean_mass = mean(body_mass_g, na.rm = TRUE),
    max_flipper_length = max(flipper_length_mm, na.rm = TRUE),
    percent_female = sum(sex == "female", na.rm = TRUE)/sum(!is.na(sex))
    )
```

  ----------- ----------- ----- ------------------------ --------------------------------- -----------------------------
  species     island      n     mean_mass               max_flipper_length                 percent_female
  Adelie      Biscoe      44    3709.65909090909         203                               0.5
  Adelie      Dream       56    3688.39285714286         208                               0.490909090909091
  Adelie      Torgersen   52    3706.37254901961         210                               0.51063829787234
  Chinstrap   Dream       68    3733.08823529412         212                               0.5
  Gentoo      Biscoe      124   5076.0162601626          231                               0.487394957983193
  ----------- ----------- ----- ------------------------ --------------------------------- -----------------------------

# References

-   UT Austin DSC385
