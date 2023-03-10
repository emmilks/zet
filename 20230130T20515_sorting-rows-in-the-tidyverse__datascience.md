---
title: sorting rows in the tidyverse
date: 01-30-2023
tags: [datascience, tidyverse]
---

``` {R}
library(palmerpenguins)
library(dplyr)

penguins |>
  arrange(bill_length_mm) |>
  head()
```

  --------- ----------- ----------------------------- ---------------------------- -------------------------------- ------------------------------ -------- ------
  species   island      `bill_length_mm`   `bill_depth_mm`   `flipper_length_mm`   `body_mass_grams`   sex      year
  Adelie    Dream       32.1                          15.5                         188                              3050                           female   2009
  Adelie    Dream       33.1                          16.1                         178                              2900                           female   2008
  Adelie    Torgersen   33.5                          19                           190                              3600                           female   2008
  Adelie    Dream       34                            17.1                         185                              3400                           female   2008
  Adelie    Torgersen   34.1                          18.1                         193                              3475                                    2007
  Adelie    Torgersen   34.4                          18.4                         184                              3325                           female   2007
  --------- ----------- ----------------------------- ---------------------------- -------------------------------- ------------------------------ -------- ------

# References

-   UT Austin DSC385
