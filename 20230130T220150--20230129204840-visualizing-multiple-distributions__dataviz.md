```{=org}
#+filetags:   :dataviz:
```
```{=org}
#+identifier: 20230130T220150
```
# Visualizing Multiple Distributions {#visualizing-multiple-distributions-1}

Visualizing multiple distributions can be tricky if you do not want to
confuse your audience. In general, histograms and kernel density plots
are a poor choice when you need to visualize multiple distributions. The
results are messy and difficult to read.

One way to solve this problem is to give each distribution its own
panel, but it is difficult to compare distributions. This is especially
true when you have more than two distributions.

## Boxplot

The best thing to do is go back to basics and use boxplots.

A box plot is read as follows:

-   The top and bottom of the box are the first and third quartiles.
-   The line in the box is the median.
-   The ends of the whiskers are either the min,max of the data or the
    lower,upper fence. The fence is defined by 1.5 \* the interquartile
    range.
-   The dots are outliers.

## Violen Plot

An extension of the boxplot is the violen plot. The violen plot gives
you a density estimate similar to the kernel density estimate plot. The
only difference is that the violen plot rotates the density plot 90
degrees and mirrors it across the y-axis.

Violen plots are the most effective when you have a lot of data points.
For small datasets, you can use a strip chart. A strip chart allows you
to see the raw data instead of an abstact representation. Horizonatal
jittering may be necessary to avoid overlapping points.

## Sina Plot

You can combine a strip chart with jittering and a violen plot to get a
sina plot. The jittered points are in proportion to the violen.

## Ridgeline Plot

Ridgeline plots are vertically staggered density plots. They provide an
artistic representation of the dataset. These plots are helpful at
showing trends in the dataset across multiple distributions.

# References

-   UT Austin DSC385
