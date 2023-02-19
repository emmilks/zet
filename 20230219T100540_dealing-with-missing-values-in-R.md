---
title: dealing with missing values in R
date: 02-19-2023
tags: [datascience tidyverse]
---

R will always return a result of NA if there is even one NA in a vector.
Use `is.na()` to check for missing values in a vector. Most R
functions include an option `na.rm` to remove NA\'s before calculating
the result.

There are several missing values of different types:

-   `NA`: logical constant indicating a missing value
-   `NA_integer_`: missing integer
-   `NA_real_`: missing real number
-   `NA_complex_`: missing complex value
-   `NA_character_`: missing string

## Type Matters

Returns 2 numbers and an NA

``` {r}
c(1, 2, NA)
```

Returns 2 numbers and an NA

``` {r}
c(1,2, NA_real_)
```

Coerces numbers to a string representation

``` {r}
c(1, 2, NA_character_)
```

This will result in a type mismatch

``` {r}
if_else(TRUE, "result if true", NA)
```

This will behave as expected.

``` {r}
if_else(TRUE, "result if true", NA_character_)
```

## Dealing with NA

Replace NAs with empty strings in a single column

``` {r}
band_data |>
  mutate(plays = replace_na(plays, ""))
```

Replace NAs with empty strings in all columns

``` {r}
band_data |>
  mutate(across(everything(), ~replace_na(.x, "")))
```

Replace empty strings with NA in a single column

``` {r}
library(naniar)
band_data |>
  replace_with_na_at("plays", ~.x == "")
```

Replace empty strings with NA in all columns

``` {r}
library(naniar)
band_data |>
  replace_with_na_all("plays", ~.x == "")
```

Removing all rows with any NAs

``` {r}
band_data |>
  na.omit()
```

Remove all rows where specific columns contain NAs

``` {r}
band_data |>
  filter(!is.na(plays))
```

Conversely

``` {r}
band_data |>
  filter(is.na(plays))
```

## Visualizing NAs

``` {r}
library(naniar)
library(ggplot2)

ggplot(NCbirths) +
  aes(Weeks, Gained) +
  geom_miss_point()
```
