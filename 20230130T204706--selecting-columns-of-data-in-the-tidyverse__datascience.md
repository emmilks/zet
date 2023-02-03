```{=org}
#+filetags:   :datascience:
```
```{=org}
#+identifier: 20230130T204706
```
``` {.r org-language="R"}
library(palmerpenguins)
library(dplyr)

penguins |>
  select(species, island, bill_length_mm) |>
  head()
```

  --------- ----------- -----------------------------
  species   island      `bill_length_mm`{.verbatim}
  Adelie    Torgersen   39.1
  Adelie    Torgersen   39.5
  Adelie    Torgersen   40.3
  Adelie    Torgersen   
  Adelie    Torgersen   36.7
  Adelie    Torgersen   39.3
  --------- ----------- -----------------------------

# References

-   UT Austin DSC385
