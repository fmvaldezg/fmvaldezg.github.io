---
title: "Homicides in Ecuador - Year 2024" 
date: 2024-04-31
lastmod: 2024-05-08
tags: ["GIS","mapping","webmap","Ecuador"]
author: ["Felipe Valdez"]
description: "Un mapa que muestra la ubicación de homicidios en Ecuador desde enero hasta abril de 2024" 
summary: "Este mapa muestra la ubicación de homicidios en Ecuador desde enero hasta abril de 2024. Cuando se aleja la vista, se muestra un mapa de calor que indica la concentración de eventos. Al acercarse a ciudades específicas, cada punto representa un evento. Los puntos están codificados por colores según el tipo de arma utilizada."

cover:
    image: "/projects/homec24/homec24.png"
    alt: "Map of Ecuador"
    relative: false
editPost:
    URL: "https://github.com/fmvaldezg/HomicidiosEC2024"
    Text: "GitHub repository"
showToc: true
disableAnchoredHeadings: false

---

## Introducción

Desde el año 2020, Ecuador experimentó un aumento significativo en el número de muertes violentas debido a varios factores, principalmente el deterioro de la economía causado por la caída de los precios del petróleo y la pandemia de COVID-19, así como el desfinanciamiento de políticas públicas relacionadas con el desarrollo social.

En Ecuador, como en otros países de la región, la disponibilidad de datos sobre este tema es escasa o inexistente. La continuidad y consistencia de los datos varía según la disposición de los funcionarios actuales. Por ejemplo, en el portal de datos abiertos [Datos abiertos](https://www.datosabiertos.gob.ec/), se pueden encontrar dos conjuntos de datos de homicidios para los años 2022 y 2024. Sin embargo, los campos y detalles no son consistentes.

Este mapa utiliza algunos de los datos disponibles en esta plataforma para mostrar algunas formas en que estos pueden ser visualizados y analizados para la toma de decisiones.

---

## El mapa

<iframe
  src="https://fmvaldezg.github.io/HomicidiosEC2024/"
  style="width:100%; height:650px;"
></iframe>

El mapa fue construido utilizando las bibliotecas Mapbox GL JS y Mapbox Assembly para el estilo.

El mapa muestra dos visualizaciones de la ubicación de eventos de homicidio desde enero hasta abril de 2024. Hasta el nivel de zoom 9 (provincias), el mapa muestra un mapa de calor que ilustra la densidad de los eventos. Esto permite al usuario identificar puntos de concentración y acercarse a ellos. Más allá del nivel de zoom 9, el mapa de calor se transforma en puntos de diferentes colores que muestran la ubicación de cada evento.

<figure style="display: inline-block; text-align: center;">
  <figcaption>Zoom Out</figcaption>
  <img src="/projects/homec24/zoomout.png" alt="zoom out" style="display:inline; width:300px; height:auto; vertical-align: middle;">
</figure>

<figure style="display: inline-block; text-align: center;">
  <figcaption>Zoom In</figcaption>
  <img src="/projects/homec24/zoomin.png" alt="zoom in" style="display:inline; width:300px; height:auto; vertical-align: middle;">
</figure>


Los puntos están coloreados según el tipo de arma utilizada. En el lado izquierdo del mapa web, hay una leyenda que incluye una representación simplificada de los colores del mapa de calor, los colores de los puntos según el tipo de arma, instrucciones breves y la fuente.

![](/projects/homec24/key.png)

Esta leyenda puede ser contraída para aumentar el área de visualización, lo que mejora la usabilidad del mapa en dispositivos móviles.

Haga clic [aquí](https://felipevaldez.com/HomicidiosEC2024/) para ver el mapa en pantalla completa.

---

## El proceso



---

## Algunas observaciones

