---
title: "Homicides in Ecuador - Year 2024" 
date: 2024-04-30
lastmod: 2024-05-08
tags: ["GIS","mapping","webmap","Ecuador"]
author: ["Felipe Valdez"]
description: "A map showing the location of homicides in Ecuador from January to April 2024" 
summary: "This map displays the location of homicides in Ecuador from January to April 2024. When zoomed out, a heatmap displaying the concentration of events is showed. When zoomed in to specific cities each point represents an event. Points are color coded base don the type of weapon used." 
cover:
    image: "/projects/homec24/homec24.png"
    alt: "Map of Ecuador"
    relative: false
editPost:
    URL: "https://github.com/fmvaldezg/HomicidiosEC2024"
    Text: "GitHub repository"
showToc: true
disableAnchoredHeadings: false
draft: false

---

## Introduction

Starting in 2020, Ecuador experienced a significant increase in the number of violent deaths due to various factors, mainly the deterioration of the economy caused by the fall in oil prices and the COVID-19 pandemic, as well as the defunding of public policy related to social development. 

In Ecuador, as in other countries in the region, the availability of data on this topic is scarce or nonexistent. The continuity and consistency of the data vary according to the willingness of the current officials. For example, on the open data portal [Datos abiertos](https://www.datosabiertos.gob.ec/) , two sets of homicide data can be found for the years 2022 and 2024. However, the fields and details are not consistent. 

This map uses some of the data available on this platform to show some ways in which these can be visualized and analyzed for decision-making.

---

## The Map

<iframe
  src="https://fmvaldezg.github.io/HomicidiosEC2024/"
  style="width:100%; height:650px;"
></iframe>

The map was build using Mapbox GL JS libraries and Mapbox Assembly for styling.

The map displays two visualizations of the location of homicide events from January to April 2024. Up to zoom level 9 (provinces), the map shows a heat map that illustrates the density of the events. This allows the user to identify concentration points and zoom in on them. Beyond zoom level 9, the heat map transitions to points of different colors that show the location of each event. 

<figure style="display: inline-block; text-align: center;">
  <figcaption>Zoom Out</figcaption>
  <img src="/projects/homec24/zoomout.png" alt="zoom out" style="display:inline; width:300px; height:auto; vertical-align: middle;">
</figure>

<figure style="display: inline-block; text-align: center;">
  <figcaption>Zoom In</figcaption>
  <img src="/projects/homec24/zoomin.png" alt="zoom in" style="display:inline; width:300px; height:auto; vertical-align: middle;">
</figure>


The points are colored based on the type of weapon used. On the left side of the web map, there is a legend that includes a simplified representation of the heat map colors, the colors of the points according to the type of weapon, brief instructions, and the source. 

![](/projects/homec24/key.png)

This legend can be collapsed to increase the viewing area, which improves the usability of the map on mobile devices.

Click [here](https://fmvaldezg.github.io/HomicidiosEC2024/) to see the map in full screen.


---

## The process



---

## Some insights

