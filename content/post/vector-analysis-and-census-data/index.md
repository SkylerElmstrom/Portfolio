---
title: Vector Analysis and Census Data
subtitle: Formatting Data, Field Calculator, and Areal Weighted Interpolation
date: 2017-10-31T19:35:41.388Z
draft: false
featured: false
tags:
  - Areal Interpolation
  - Census
  - GIS
  - ArcGIS
  - Spatial Analysis
image:
  filename: featured
  focal_point: Smart
  preview_only: false
---
In this lesson, I learned how to download Census.gov data and format tabular demographic data to my needs. We applied ***Table Joins*** from the tabular data to our geographic data and used the ***Field Calculator*** to calculate new fields as necessary. Using ***Dissolve*** and ***Calculate Geometry***, we created polygons for storing future predictions of local school district enrollment. We also used proximity and analysis tools to create a map of the US broken into areas closest to a national park.

### Enrollment Change Predictions

> * Assess future changes in enrollment in Bellingham elementary schools
> * Compile census dataset that shows the number of young children (ages 5-9) currently in each school attendance and the number of potential future students (age <5)
> * Map the likely enrollment change

Spatial data from the City of Bellingham provided me with attendance zones to use alongside my census data. In order to get an accurate measure of how many students live in a particular zone per unit area, I ***Erased*** areas with water-bodies, glaciers, and other features where people do not live from my census and attendance zone data. Finally, I used the ***Intersect*** tool to combine my datasets and calculate enrollment based on weighted areas within the attendance zones. The weights were created for each census block group based on area to account for them being split between attendance zone polygons.

![Map of Bham School District Expected Change in Enrollment](elmstrom_lab3_map3.png "Bellingham School District Expected Change in Enrollment")

### National Park Proximity Map

This map was a test of acquired skills in previous lessons. I created it using voronoi (euclidean distance) polygons between each national park in the US, similar to the map found [here](https://www.reddit.com/r/MapPorn/comments/21yoxe/voronoi_map_of_national_parks_the_usa_divided/) but with a few more cartographic refinements.

![Map of US National Park Proximity](elmstrom_exam2.png "Map of US National Park Proximity")