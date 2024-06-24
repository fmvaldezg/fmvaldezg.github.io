---
title: "Fires in Quito - August 2023" 
date: 2023-09-31
lastmod: 2023-10-08
tags: ["GIS","mapping","webmap","Ecuador", "Quito", "fire"]
author: ["Felipe Valdez"]
description: "A map showing the location of fires detected by satellite imegery in Quito." 
summary: "This map shows the location of fires detected using satellite imagery in Quito during August 2023." 
cover:
    image: "/projects/firesuio23/firesuio23.png"
    alt: "Map of Quito with red spots"
    relative: false
editPost:
    URL: "https://github.com/fmvaldezg/Quito_Fires2023"
    Text: "GitHub repository"
showToc: true
disableAnchoredHeadings: false

---

## Introduction

During the dry season (June - August), fires are often frequent in the Andean region of Ecuador, especially near the cities. In the year 2023, an unusual number of fires occurred near Quito, some of which suspiciously started at night. 
This map uses data from [NASA FIRMS](https://firms.modaps.eosdis.nasa.gov/) (Fire Information for Resource Management System) and shows a time animation of the fire events from August 1 to September 19, 2023. 
The map allows filtering of the events based on the time of occurrence, day/night.

---

## The Map

<iframe
  src="https://fmvaldezg.github.io/Quito_Fires2023/"
  style="width:100%; height:650px;"
></iframe>

The map was build using Mapbox GL JS libraries and Mapbox Assembly for styling.

The map shows the location of fire events according to heat points (above 200 degrees Kelvin) in the Visible Infrared Imaging Radiometer Suite (VIIRS) images. The color and size of the markers are defined by the brightness of the event. 

The map has a default animation that progresses through the dates and displays the events cumulatively. The animation can be paused and resumed at any time. The timeline indicator can be grabbed and moved to a specific moment. 

The three buttons allow filtering for "all" events, or only those that occurred during the "day" or "night."


Click [here](https://fmvaldezg.github.io/Quito_Fires2023/) to see the map in full screen.


---

## The process



---

## Some insights

