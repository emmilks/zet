---
title: color scales
date: 01-29-2023
tags: [dataviz]
---

# Color Scales

There are four uses of color in data visualization.

1.  Distinguish categories (qualitative)
    -   Orderless
    -   Even colors. Do not highlight one category over the others.
2.  Represent numeric values (sequential scale)
    -   Ordered
    -   **Perceptually uniform**. Each step looks like the same size as
        the previous step.
3.  Represent numeric data (diverging scale)
    -   two sequential scales that meet in the middle.
    -   correlation coefficient is an example
4.  Highlight
    -   Make certain data values stand out from the rest of the values.

Your choice of color scale can create a very different impression and
you can highlight certain aspects of the plot or not. Pick an
appropriate color scale for each of these four categories or you could
confuse or mislead your audience.

## `ggplot2` Color Scale Functions are a Mess

This table is not exhaustive.

  scale function                         aesthetic   data type    palette type
  -------------------------------------- ----------- ------------ ------------------------------------
  `scale_color_hue()`         color       discrete     qualitative
  `scale_fill_hue()`          fill        discrete     qualitative
  `scale_color_gradient`      color       continuous   sequential
  `scale_color_gradient2`     color       continuous   divergent
  `scale_fill_viridis_c()`    color       continuous   sequential
  `scale_fill_viridis_d()`    fill        discrete     sequential
  `scale_color_brewer()`      color       discrete     qualitative, sequential, divergent
  `scale_fill_brewer()`       fill        discrete     qualitative, sequential, divergent
  `scale_color_distiller()`   color       continuous   qualitative, sequential, divergent

The `colorspace` package creates some order out of the ggplot
mess.

Scale name: `scale_<aesthetic>_<datatype>_<colorscale>()`

-   aesthetic: fill, color
-   datatype: discrete, continuous, binned (histogram with color)
-   colorscale: qualitative, sequential, diverging, divergingx

## Discrete, Qualitative Scale

This scale is best set manually. `ggplot` could do a poor job
choosing the colors. If you have more than eight categories then trying
to encode them in color is the wrong approach. Use facets instead.
Typically use three to four colors in a single plot

# References

-   UT Austin DSC385
