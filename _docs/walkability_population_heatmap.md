---
title: Walkability Population Heatmap
permalink: /docs/walkability population heatmap/
---

In addition to the [Walkability Heatmap](https://www.open-accessibility.org/docs/heatmap/), GOAT allows you to visualize another heatmap called Walkability Population Heatmap. This heatmap gives a better understanding of the accessibility in a specific area or neighborhood based on its population. The walkability population heatmap can be used to answer many planning questions. Among them:
- where can an accessibility surplus be found in the studied neighborhood?
- where can a density surplus be found in the studied neighborhood?
- where is densification needed? 
- where is the improvement of the accessibility to specific amenity or public transport stations needed?

{% include image.html src="docs/technical_documentation/walkability_population_index/walkability_population_map.png" %}

#### 1. Calculation
The layer of walkability population is the result of the intersection of the two layers walkability and population. 
{% include image.html src="docs/technical_documentation/walkability_population_index/intersection_2_layers.png" %}

#### 2. Classification
In order to classify the accessibility levels that were computed for each grid cell, a classification based on percentile is used. The following table shows how the percentiles of accessibility and population are calculated in each grid.

{% include image.html src="docs/technical_documentation/walkability_population_index/percentile.png" %}

The population accessibility is calculated as following:

<b> Population-Accessibility = Percentile_Population – Percentile_Accessibility </b>

and shows following result:
{% include image.html src="docs/technical_documentation/walkability_population_index/calculated_index.png" maxheight="150px" %}


