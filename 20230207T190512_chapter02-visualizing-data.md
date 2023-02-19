---
title: chapter02 visualizing data
date: 02-07-2023
tags: [dataviz]
---

# Visualizing Data

Data visualization is about taking data and mapping it to a picture in
a logical way that captures what the data is doing. Data visualization can be
thought of as a language with its own grammar that helps us understand what the
underlying data values mean.

Aesthetics describe every graphical element in the visualization. Common
aesthetics include:

* position
* color
* size
* shape
* line type
* line width

If text is included as part of the visualization, then we have to consider
the font type and font size.

Data can be split broadly into two groups: continuous and discrete.

    * **continuous data** - can be represented by the real numbers. Position,
      size, color, and line width can represent continuous data.
    * **discrete data** - can be represented by the integers. Shape and line
      type can be used to represent discrete data.

Data an come in the form of discrete categories, text, dates, or times.

    * **quantitative** - data is numerical
    * **qualitative** - data is categorical. These variables are referred to as
      factors in R and the categories are called levels.

## Scales Map Data onto Aesthetics

A scale defines a unique mapping between data and aesthetics. A scale must be
one-to-one otherwise the visualization becomes ambiguous.

Discrete position scales: the levels of the factor are evenly spaced along the
axis, ordered factors are placed in order along the axis, unordered factors can
be placed at the discretion of the analyst

## References

Wilkes, *Fundamentals of Data Visualization*
