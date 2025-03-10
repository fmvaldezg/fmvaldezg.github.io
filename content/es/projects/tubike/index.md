---
title: "Temple University Bike Tour - Animated Map"
date: 2024-04-28
lastmod: 2024-05-08
tags: ["webmap","animated","mapbox"]
author: "Felipe Valdez"
description: "Un mapa animado de la ruta del Tour en Bicicleta de la Universidad de Temple 2024" 
summary: "Este mapa muestra una ruta animada del tour sobre una imagen satelital. La ventana emergente sobre el marcador muestra la distancia recorrida" 
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

## El Tour

El 28 de abril, la Universidad de Temple organizó un recorrido en bicicleta de 22 millas desde el Campus Principal en Filadelfia hasta Temple Ambler.

[Más información sobre el Tour](https://ambler.temple.edu/community/temple-university-bike-tour)

---

## Mapa animado

<iframe
  src="https://fmvaldezg.github.io/bike-rideTU/"
  style="width:100%; height:400px;"
></iframe>



<div style="line-height: 1.8;">
El mapa muestra un marcador que sigue la ruta del tour sobre una imagen satelital. A medida que avanza la ruta, una línea rojiza marca el camino recorrido. Una ventana sobre el marcador indica la distancia cubierta desde el punto de origen <a href="https://www.temple.edu/">Campus Principal de la Universidad de Temple</a> hasta la ubicación del marcador. La animación comienza automáticamente cuando se carga la página pero puede ser pausada <img src="/projects/tubike/play.png" alt="Botón de Pausa" style="display:inline; width:30px; height:auto; vertical-align: middle;"> o reiniciada <img src="/projects/tubike/rest.png" alt="Botón de Reinicio" style="display:inline; width:30px; height:auto; vertical-align: middle;"> usando los botones en la esquina superior derecha.
</div>





<br></br>
Haga click [aquí](https://fmvaldezg.github.io/bike-rideTU/) para ver el mapa en pantall completa.


---

## El proceso

El mapa fue construido utilizando las bibliotecas Mapbox GL JS, Mapbox Assembly para el estilo y Turf para recuperar y calcular la distancia.

1. Se descargó un archivo .gpx desde [aquí](https://web.archive.org/web/20240416173144/https://www.mapmyride.com/routes/view/5385860881).
2. El archivo .gpx fue convertido a formato Geojson utilizando QGIS.
3. Se creó un archivo HTML básico para iniciar el mapa siguiendo los [ejemplos](https://docs.mapbox.com/mapbox-gl-js/example/) de Mapbox en su web.
4. Se añadieron los logos de la Universidad de Temple a los puntos de inicio y fin del tour.
5. El código y los datos fueron alojados en github y desplegados usando github pages.

### Configuraciones

+ Utilizamos el `satellite-streets-v12` como mapa base.
+ Utilizamos `path = turf.lineString()` y `pathDistance = turf.lineDistance(path)` para obtener la distancia total.
+ El `const alongPath = turf.along(path, distanceTraveled).geometry.coordinates;` recupera latitud y longitud en la ruta.



---




