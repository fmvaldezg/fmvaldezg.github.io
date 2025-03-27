---
title: "Incendios en Quito - August 2023" 
date: 2023-09-31
lastmod: 2023-10-08
tags: ["GIS","mapping","webmap","Ecuador", "Quito", "fire"]
author: ["Felipe Valdez"]
description: "Un mapa que muestra la ubicación de incendios detectados por imágenes satelitales en Quito." 
summary: "Este mapa muestra la ubicación de incendios detectados mediante imágenes satelitales en Quito durante agosto de 2023." 
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

## Introducción

Durante la estación seca (junio - agosto), los incendios son frecuentes en la región andina de Ecuador, especialmente cerca de las ciudades. En el año 2023, ocurrió un número inusual de incendios cerca de Quito, algunos de los cuales comenzaron sospechosamente durante la noche.

Este mapa utiliza datos de [NASA FIRMS](https://firms.modaps.eosdis.nasa.gov/) (Sistema de Información de Incendios para Gestión de Recursos) y muestra una animación temporal de los eventos de incendios desde el 1 de agosto hasta el 19 de septiembre de 2023.

El mapa permite filtrar los eventos según la hora de ocurrencia, día/noche.

---

## El mapa

<iframe
  src="https://fmvaldezg.github.io/Quito_Fires2023/"
  style="width:100%; height:650px;"
></iframe>

El mapa fue construido utilizando las bibliotecas Mapbox GL JS y Mapbox Assembly para el estilo.

El mapa muestra la ubicación de eventos de incendios según puntos de calor (por encima de 200 grados Kelvin) en las imágenes del Visible Infrared Imaging Radiometer Suite (VIIRS). El color y tamaño de los marcadores están definidos por el brillo del evento.

El mapa tiene una animación predeterminada que avanza a través de las fechas y muestra los eventos de forma acumulativa. La animación puede ser pausada y reanudada en cualquier momento. 

El indicador de línea de tiempo puede ser arrastrado y movido a un momento específico.

Los tres botones permiten filtrar por eventos "todos", o solo aquellos que ocurrieron durante el "día" o la "noche".
Haga clic [aquí](https://felipevaldez.com/Quito_Fires2023/) para ver el mapa en pantalla completa.


---

## El proceso



---

## Algunas observaciones

