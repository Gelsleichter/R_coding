---
# Title, summary, and page position.
linktitle: Chapter 1
summary: Learn how to use Wowchemy's docs layout for publishing online courses, software documentation, and tutorials.
weight: 1
icon: book
icon_pack: fas

# Page metadata.
title: Data Manipulation 
date: '2018-09-09T00:00:00Z'
type: book # Do not modify.
---

## Data Manipulation with **dplyr**

The dplyr package in R is a powerful tool for data manipulation that provides a consistent set of verbs to help simplify complex data manipulation tasks. In this example, we use the mtcars dataset, which is readily available in R, to demonstrate filtering, selecting specific columns, grouping, and summarizing data.

```R
# Load the dplyr package for data manipulation
library(dplyr)

# Data manipulation using the mtcars dataset
mtcars %>%
  filter(mpg > 20) %>%  # Filter rows where miles per gallon (mpg) is greater than 20
  select(mpg, cyl, wt) %>%  # Select columns: mpg, number of cylinders (cyl), and weight (wt)
  group_by(cyl) %>%  # Group data by the number of cylinders
  summarise(
    avg_mpg = mean(mpg),  # Calculate average mpg for each group of cylinders
    avg_wt = mean(wt)  # Calculate average weight for each group of cylinders
  )
# This code filters cars with more than 20 mpg, selects relevant columns, groups by cylinder count,
# and then calculates the average mpg and weight for each group.
```

