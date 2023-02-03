---
title: wrangling data in the tidyverse
date: 01-30-2023
tags: [datascience]
---

# Wrangling Data in the Tidyverse

Data wrangling is the process of performing operations on a dataset that
change it some way in order to answer questions or clean it up for
future analysis. Data in the real world is often messy and not fit for
analysis in its raw form.

## Elementary Data Manipulations

  Operation        Tidyverse Function
  ---------------- -------------------------------------------------------------------------------
  Pick rows        `filter()`
  Pick columns     `select()`
  Sort rows        `arrange()`
  Count things     `count()`
  Add columns      `mutate()`
  Analyze          `group_by()` and `summarize()`
  Reshape          `pivot_wider()` and `pivot_longer()`
  Combine tables   `left_join()`, `inner_join()`, `full_join()`

`%>%` and `|>` are the pipe operators. Output from
the first function is fed as input nto the second function. It can be
read as \"and then\".

Links to data manipulation functions:

[filtering data in the tidyverse](denote:20230130T204205)

[selecting columns of data in the tidyverse](denote:20230130T204706)

[sorting rows in the tidyverse](denote:20230130T205152)

[counting data in the tidyverse](denote:20230130T205409)

[adding columns to an existing dataset in the
tidyverse](denote:20230130T205704)

[pivot tables in the tidyverse](denote:20230130T210039)

[reshaping data in the tidyverse](denote:20230130T211410)

[combining datasets in the tidyverse](denote:20230130T213204)

# References

-   UT Austin DSC385
