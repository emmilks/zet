```{=org}
#+filetags:   :dataviz:
```
```{=org}
#+identifier: 20230130T221127
```
# Wrangling Data in the Tidyverse {#wrangling-data-in-the-tidyverse-1}

Data wrangling is the process of performing operations on a dataset that
change it some way in order to answer questions or clean it up for
future analysis. Data in the real world is often messy and not fit for
analysis in its raw form.

## Elementary Data Manipulations

  Operation        Tidyverse Function
  ---------------- -------------------------------------------------------------------------------
  Pick rows        `filter()`{.verbatim}
  Pick columns     `select()`{.verbatim}
  Sort rows        `arrange()`{.verbatim}
  Count things     `count()`{.verbatim}
  Add columns      `mutate()`{.verbatim}
  Analyze          `group_by()`{.verbatim} and `summarize()`{.verbatim}
  Reshape          `pivot_wider()`{.verbatim} and `pivot_longer()`{.verbatim}
  Combine tables   `left_join()`{.verbatim}, `inner_join()`{.verbatim}, `full_join()`{.verbatim}

`%>%`{.verbatim} and `|>`{.verbatim} are the pipe operators. Output from
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
