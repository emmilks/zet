---
title: visualizing proportions using ggplot2
date: 02-01-2023
tags: [dataviz]
---

The most common way to visualize proportions is the pie chart.

INSERT R code

The other way to visualize proportions is to use b are charts.

STACKED BAR CHART

The total size of the data is represented as the height of the bar and
this single bar is broken down into subgroups.

STAGGERED BAR CHART

The bars together sum up to 100% of the data. This makes it easy to
compare relative amounts.

## Pros and Cons of these Approaches

                                             Pie Chart   Stacked Bar Chart   Staggered Bar Chart
  ------------------------------------------ ----------- ------------------- ---------------------
  Easy comparisons of relative proportions   no          no                  yes
  Shows data as proportions of the whole     yes         yes                 no
  Emphasizes simple fractions                yes         no                  no
  Visually appealing for small datasets      yes         no                  yes
  Works well for large numbers of subsets    no          no                  yes
  Works well for time series and similar     no          yes                 no

No one visualization fits for all scenarios. Pick the one that works
best for your situation.

## Nested Proportions

- **Mosaic plots**: subdivides data into two dimensions.
- **Treemap plots**: the second dimension is merged into the rectangle and
  represented as the area of the rectangle.
- **Parallel set plots**: can show many subdivisions at once. The bands show
  how \*things are related.
