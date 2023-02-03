---
title: reshaping data in the tidyverse
date: 01-30-2023
tags: [datascience, tidyverse]
---

Long format data is better for machines and doing analysis. Wide format
data is better for humans. It is more intuitive and easier to read. It
is common, as a data analyst, that you will receive data in a wide
format and you will need to convert it to a long format in order to do
your analysis. After the analysis, you should convert the data back into
a wide format for the report so your manager doesn\'t have to think to
hard.

``` {r}
library(palmerpenguins)
library(tidyverse)

# Reshape the data
penguins_wide <- penguins |>
  count(species, island) |>
  pivot_wider(names_from = "island", values_from = "n")

```

  ----------- -------- ------- -----------
  species     Biscoe   Dream   Torgersen
  Adelie      44       56      52
  Chinstrap            68
  Gentoo      124
  ----------- -------- ------- -----------

``` {r}
# Make it longer again
penguins_wide |>
  pivot_longer(cols = -species, names_to = "island", values_to = "n")
```

  ----------- ----------- -------
  species     island      count
  Adelie      Biscoe      44
  Adelie      Dream       56
  Adelie      Torgersen   52
  Chinstrap   Biscoe
  Chinstrap   Dream       68
  Chinstrap   Torgersen
  Gentoo      Biscoe      124
  Gentoo      Dream
  Gentoo      Torgersen
  ----------- ----------- -------

# References

-   UT Austin DSC385
