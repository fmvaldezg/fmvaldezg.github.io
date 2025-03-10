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

## Introducción

En diciembre de 2023, la primera línea del metro de Quito comenzó operaciones. Cubriendo una ruta de 22 kilómetros, este es el primer sistema de transporte público subterráneo de la ciudad. [Más información](https://metrodequito.gob.ec/)

Este mapa muestra las áreas de servicio desde cada una de las 15 estaciones para caminar, andar en bicicleta y conducir. Se utilizan cuatro intervalos de tiempo de viaje: 5, 10, 15 y 20 minutos desde cada estación.

---

## El Mapa

<iframe
  src="https://fmvaldezg.github.io/ISOmetroUIO/"
  style="width:100%; height:650px;"
></iframe>

El mapa fue construido utilizando las bibliotecas Mapbox GL JS y Mapbox Assembly para el estilo.

El mapa muestra la ubicación de las 15 estaciones del metro de Quito. El usuario puede seleccionar entre tres tipos de desplazamiento: a pie, en bicicleta y en automóvil. Luego se puede seleccionar un umbral de tiempo de 5 a 20 minutos. Para visualizar el área de servicio resultante, se debe seleccionar una de las estaciones del menú desplegable.

En el mapa, un polígono rojo mostrará el área de servicio resultante para el tipo de desplazamiento y el umbral de tiempo seleccionado.

Esta herramienta ayuda a identificar brechas en la distribución de las estaciones de metro. Los siguientes pasos incluyen reportar el número total de población cubierta por el área de servicio resultante.

Haga clic [aquí](https://fmvaldezg.github.io/ISOmetroUIO/) para ver el mapa en pantalla completa.

---

## El proceso

Las isócronas de áreas de servicio se generan utilizando la [API de Isócrona de Mapbox](https://docs.mapbox.com/api/navigation/isochrone/).

Las dos primeras secciones de botones establecen los parámetros que completan la llamada a la API `profile` y `contours_minutes`.
El parámetro `coordinates` de la llamada se obtiene de un archivo geojson que almacena las ubicaciones de las estaciones, después de que el usuario selecciona una del menú desplegable. Las estaciones en el menú desplegable están listadas de norte a sur.

Este es el primer proyecto que utiliza Mapbox GL JS Standard Style y la propiedad `slot: 'middle'` para colocar los polígonos debajo de los edificios y encima de las calles.

---

## Algunas observaciones