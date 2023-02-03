```{=org}
#+filetags:   :datascience:
```
```{=org}
#+identifier: 20230130T205409
```
``` {.r org-language="R"}
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
