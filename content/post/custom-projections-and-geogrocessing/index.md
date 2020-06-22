---
title: Custom Projections and Geogrocessing
subtitle: Features Proximity Tools, Location Selection, and Model Builder
date: 2020-06-22T22:34:58.631Z
draft: true
featured: false
image:
  filename: yellowstone.png
  focal_point: Smart
  preview_only: false
---
This lesson was designed to explore distortions of distance and area by different projections, examining geospatial metadata, customizing a projection for a map, and using geoprocessing tools to identify features within a specified distance of some other feature.

## Yellowstone

Our task was simple:

> Evaluate projections of existing data and reproject if necessary\
> Produce a map of USGS ash fall predictions during a hypothetical Yellowstone Caldera eruption\
> Identify all the cities within 500 km of the caldera that may receive greater than 1 cm of ash fall

ArcMap allows the user to define their own projections. In my case, I wanted to define the extent of my equal area projection in order to reduce distortion around my subject area (Yellowstone).  I extracted cities using a 500 km buffer around the centroid of the caldera and the SELECT BY LOCATION tool to create a new feature class containing the affected cities. Although the task only asked for cities within 500 km of the caldera, I wanted to show the actual ash fall predictions on my map. I converted tabular prediction data from the USGS project into a classified raster for visualizing the modeled ash fall.

![](yellowstone.png)