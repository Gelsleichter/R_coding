---
# Title, summary, and page position.
linktitle: Data Visualization
summary: Learn a bit of data visualization with dplyr R package.
weight: 1
icon: book
icon_pack: fas

# Page metadata.
title: Data Visualization 
date: '2018-09-09T00:00:00Z'
type: book # Do not modify.
---

## Data Visualization with **ggplot2**

The ggplot2 package is a versatile tool for creating complex and aesthetically pleasing visualizations. Here, we create a scatter plot to examine the relationship between car weight (wt) and miles per gallon (mpg), using the number of gears (gear) to color-code the points, which adds additional layer of information to the plot.

```R
# Load the ggplot2 package for advanced data visualization
library(ggplot2)

# Create a scatter plot with ggplot2
ggplot(mtcars, aes(x = wt, y = mpg, color = factor(gear))) +  # Define aesthetics: map wt to x, mpg to y, and gear to color
  geom_point() +  # Add points to represent each car
  theme_minimal() +  # Use a minimalistic theme for a clean look
  labs(title = "MPG vs. Car Weight, Colored by Number of Gears",  # Add a plot title
       x = "Car Weight (1000 lbs)",  # Label the x-axis
       y = "Miles per Gallon",  # Label the y-axis
       color = "Number of Gears")  # Add a legend title for gear colors
# This visualization helps in understanding how both weight and the number of gears relate to a car's fuel efficiency.

```
