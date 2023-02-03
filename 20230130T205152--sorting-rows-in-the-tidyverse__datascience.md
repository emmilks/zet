```{=org}
#+filetags:   :datascience:
```
```{=org}
#+identifier: 20230130T205152
```
``` {.r org-language="R"}
library(palmerpenguins)
library(dplyr)

penguins |>
  arrange(bill_length_mm) |>
  head()
```

  --------- ----------- ----------------------------- ---------------------------- -------------------------------- ------------------------------ -------- ------
  species   island      `bill_length_mm`{.verbatim}   `bill_depth_mm`{.verbatim}   `flipper_length_mm`{.verbatim}   `body_mass_grams`{.verbatim}   sex      year
  Adelie    Dream       32.1                          15.5                         188                              3050                           female   2009
  Adelie    Dream       33.1                          16.1                         178                              2900                           female   2008
  Adelie    Torgersen   33.5                          19                           190                              3600                           female   2008
  Adelie    Dream       34                            17.1                         185                              3400                           female   2008
  Adelie    Torgersen   34.1                          18.1                         193                              3475                                    2007
  Adelie    Torgersen   34.4                          18.4                         184                              3325                           female   2007
  --------- ----------- ----------------------------- ---------------------------- -------------------------------- ------------------------------ -------- ------

# References

-   UT Austin DSC385
