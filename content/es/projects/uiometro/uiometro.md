---
title: "Metro de Quito" 
date: 2023-12-31
lastmod: 2023-12-31
tags: ["GIS","mapping","webmap","Ecuador", "Quito", "transportation"]
author: ["Felipe Valdez"]
description: "A map showing service areas from each Metro Station" 
summary: "This map shows service areas from each Metro Station walking, biking and driving for times of 5 minutes, 10 minutes 15 minutes and 20 minutes." 
cover:
    image: "/projects/uiometro/uiometro.png"
    alt: "Map of Metro de Quito"
    relative: false
editPost:
    URL: "https://github.com/fmvaldezg/ISOmetroUIO"
    Text: "GitHub repository"
showToc: true
disableAnchoredHeadings: false

---

## Introduction

In December 2023, the first metro line in Quito began operations. Covering a 22-kilometer route, this is the city's first underground public transportation system. [Learn more](https://metrodequito.gob.ec/)

This map shows the service areas from each of the 15 stations for walking, cycling, and driving. Four travel time intervals are used: 5, 10, 15, and 20 minutes from each station.

---

## The Map

<iframe
  src="https://fmvaldezg.github.io/ISOmetroUIO/"
  style="width:100%; height:650px;"
></iframe>

The map was build using Mapbox GL JS libraries and Mapbox Assembly for styling.

The map shows the location of 15 stations of the Quito's subway. The user can select from three types of travelling: walking, biking and driving. Then a time threshold from 5 to 20 minutes can be selected. To visualize the resulting service area, one of the stations has to be selected fromt he dropdown menu. 

In the map, a red polygon will show the resulting service are for the type of travel and the time threshold selected.

This tool helps identify gaps in the distribution of subway stations. Next steps include reporting the total number of poulation covered by the resulting service area.


Click [here](https://fmvaldezg.github.io/ISOmetroUIO/) to see the map in full screen.


---

## The process

The service area isochrones are generated using the [Mapbox Isochrone API](https://docs.mapbox.com/api/navigation/isochrone/). 

The first two section of buttons set the parameters that populate the api call `profile` and `contours_minutes`.
The `coordinates` parameter of the call is retrieved from a geojson file that stores the station locations, after the user selects one from the dropdown menu. Stations in the dropdown menu are listed from north to south. 

This is the first project using Mapbox GL JS Standard Style and the `slot: 'middle'` property to place the polygons below the buildings and above streets. 

---

## Some insights

