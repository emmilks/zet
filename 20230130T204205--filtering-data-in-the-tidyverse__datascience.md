```{=org}
#+filetags:   :datascience:
```
```{=org}
#+identifier: 20230130T204205
```
``` {.r org-language="R"}
library(palmerpenguins)
library(dplyr)

penguins |>
  filter(species == "Gentoo") |>
  head()
```

  --------- -------- ----------------------------- ---------------------------- -------------------------------- ------------------------------ -------- ------
  species   island   `bill_length_mm`{.verbatim}   `bill_depth_mm`{.verbatim}   `flipper_length_mm`{.verbatim}   `body_mass_grams`{.verbatim}   sex      year
  Gentoo    Biscoe   46.1                          13.2                         211                              4500                           female   2007
  Gentoo    Biscoe   50                            16.3                         230                              5700                           male     2007
  Gentoo    Biscoe   48.7                          14.1                         210                              4450                           female   2007
  Gentoo    Biscoe   50                            15.2                         218                              5700                           male     2007
  Gentoo    Biscoe   47.6                          14.5                         215                              5400                           male     2007
  Gentoo    Biscoe   46.5                          13.5                         210                              4550                           female   2007
  --------- -------- ----------------------------- ---------------------------- -------------------------------- ------------------------------ -------- ------

# References

-   UT Austin DSC385
