---
title: reordering data in R
date: 02-19-2023
tags: [datascience tidyverse]
---

# Ordering Data with the `forcats` library

Getting your data in order is important because it makes it easy to
compare categories and know with one glance which category is number 1
and which is dead last.

## Manually

The `fct_relevel()` function from the `forcats`
library manually reorders the data according to the analysts wishes.

``` {r}
library(ggplot2)
library(forcats)
library(palmerpenguins)

ggplot(penguins, aes(y = fct_relevel(species, "Chinstrap", "Gentoo", "Adelie"))) +
  geom_bar()
```

It is better to act on the dataframe to prevent the `aes`
function from getting overcrowded.

``` {r}
library(tidyverse)
library(palmerpenguins)

penguins |>
  mutate(species = fct_relevel(species, "Chinstrap", "Gentoo", "Adelie")) |>
  ggplot(aes(y = species)) +
  geom_bar()
```

A factor in R gives a categorical variable defined levels with logical
ordering.

## Automatic

The `fct_infreq()` function will relevel the factors based on
the frequency of each factor in the variable. The order is descending.
`fct_rev()` does the same thing but the order is ascending.

``` {r}
library(tidyverse)
library(palmerpenguins)

penguins |>
  mutate(species = fct_infreq(species)) |>
  slice(1:30) |>
  pull(species)
```

`fct_reorder()` reorders the data based on numeric values.

``` {r}
library(tidyverse)
library(palmerpenguins)

penguins |>
  count(species) |>
  mutate(speces = fct_reorder(species, n)) |>
  pull(species)
```

### Other plot types

Reordering data is not limited to barplots. Any visualization that
involves categorical variables can be made to look better by reordering
the data. By default, ggplot will sort the variables alphabetically
which is rarely what you want. It makes the plot look messy. Use
`fct_reorder()` to sort the data by frequency to make
comparisons easier.

### Facets

Facets can be reordered as well. `fct_reorder()` uses the median by
default. It can be set explicitly. Any summary function will work. In
general, there is no rule for the correct way to reorder this type of
data. Use what makes sense for your analysis.

### Lumping factor levels together

Sometimes it is necessary to lump together less important variables
because they do not contribute much to the overall message of the plot.
If you are looking at the top flights out of NYC, do you really care
about the airlines that have hardly any flights out the city in a given
year. `fct_lump_n()` solves this problem by creating an Other
category that combines the categories that you do not care about.

It is possible to give the Other column a separate color from the rest
of the named variables.

Fix the legend ordering using `fct_rev()` or the
`scale_fill_manual()` function to explicitly set the color.
