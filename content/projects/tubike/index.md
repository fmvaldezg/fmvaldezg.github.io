---
title: "Temple University Bike Tour - Animated Map"
date: 2024-04-28
lastmod: 2024-05-08
tags: ["webmap","animated","mapbox"]
author: "Felipe Valdez"
description: "An animated map of the route of the Temple University Bike Tour 2024" 
summary: "This map displays an animated route of the tour over a satellite image. The popup window over the marker shows the traveled distance" 
cover:
    image: "/projects/tubike/tubike.png"
    alt: "Static image of a map of Philadelphia"
    relative: false
editPost:
    URL: "https://github.com/fmvaldezg/bike-rideTU"
    Text: "TU Bike Tour"
showToc: true
disableAnchoredHeadings: false

---

## The Tour

On April 28th, Temple University organized 22-mile bike tour from Main Campus in Philadelphia to Temple Ambler.  

[More Info on the Tour](https://ambler.temple.edu/community/temple-university-bike-tour)

---

## The Animated Map

<iframe
  src="https://fmvaldezg.github.io/bike-rideTU/"
  style="width:100%; height:400px;"
></iframe>



<div style="line-height: 1.8;">
The map shows a marker that follows the tour route over a satellite image. As the route progresses, a reddish line marks the path traveled. A window above the marker indicates the distance covered from the point of origin <a href="https://www.temple.edu/">Temple University Main Campus</a> to the marker's location. The animation starts automatically when the page loads but can be paused <img src="/projects/tubike/play.png" alt="Pause Button" style="display:inline; width:30px; height:auto; vertical-align: middle; "> or restarted <img src="/projects/tubike/rest.png" alt="Restart Button" style="display:inline; width:30px; height:auto; vertical-align: middle;"> using the buttons in the top right corner.
</div>





<br></br>
Click [here](https://fmvaldezg.github.io/bike-rideTU/) to see the map in full screen.


---

## The process

The map was build using Mapbox GL JS libraries, Mapbox Assembly for styling and Turf to retreive and calculate the distance. 

1. A .gpx file was dowloaded from [here](https://web.archive.org/web/20240416173144/https://www.mapmyride.com/routes/view/5385860881).
2. The .gpx file was converted to a Geojson format using QGIS.
3. A basic HTML file to initiate the map was created following Mapbox [examples](https://docs.mapbox.com/mapbox-gl-js/example/) on their web.
4. Temple University logos were added to the start and end points of the tour. 
5. The code and data were hosted in github and deployed using github pages.

### Settings

+ We used the `satellite-streets-v12` as the basemap.
+ We used `path = turf.lineString()` and `pathDistance = turf.lineDistance(path)` to get the total distance.
+ The `const alongPath = turf.along(path, distanceTraveled) .geometry.coordinates;` retrieves latitude and longitude on the path.



---




