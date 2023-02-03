---
title: combining datasets in the tidyverse
date: 01-30-2023
tags: [datascience, tidyverse]
---

We use joins to add columns from one table into another table.

-   `left_join()` - take the table on the right and merge it
    with the table on the left based on a shared column.

``` {R}
library(tidyverse)

band_members = tibble(name = c("Mick", "John", "Paul"),
                      band = c("Stones", "Beatles", "Beatles"))

band_instruments = tibble(name = c("John", "Paul", "Keith"),
                          plays = c("guitar", "bass", "guitar"))

left_join(band_members, band_instruments)
```

  ------ --------- --------
  name   band      plays
  Mick   Stones
  John   Beatles   guitar
  Paul   Beatles   bass
  ------ --------- --------

-   `right_join()` - take the table on the left and merge it
    with the table on the right based on a shared column.

    ``` {R}
    right_join(band_members, band_instruments)
    ```

  ------- --------- --------
  name    band      plays
  John    Beatles   guitar
  Paul    Beatles   bass
  Keith             guitar
  ------- --------- --------

-   `inner_join()` - keep the intersection of the two tables
    and toss out everything else.

    ``` {R}
    inner_join(band_members, band_instruments)
    ```

  ------ --------- --------
  name   band      plays
  John   Beatles   guitar
  Paul   Beatles   bass
  ------ --------- --------

-   `full_join()` - union of the two tables. All information
    is retained.

    ``` {R}
    full_join(band_members, band_instruments)
    ```

  ------- --------- --------
  name    band      plays
  Mick    Stones
  John    Beatles   guitar
  Paul    Beatles   bass
  Keith             guitar
  ------- --------- --------

**Tip**: in case of doubt, use `left_join`. It is often the
best choice for the job.

# References

-   UT Austin DSC385
