+++
author = "Jorge Hernández"
bg_image = "/images/net.jpg"
categories = ["Time series"]
date = 2022-07-05T05:00:00Z
description = "¿Cómo crear muchas estimaciones a la vez?"
image = "/images/rlogo.png"
tags = ["bucle", "Forecasting", "Time series"]
title = "Creando pronósticos masivos en bucle"
type = "post"

+++
## ¿Cómo crear muchas estimaciones a la vez?

Hace unos meses en mi trabajo comencé a hacer algunas mejoras en estimaciones de servicios por parte de la empresa, a lo cuál traté de hacer un modelo global que estimara los servicios totales que se iban a requerir en los próximos meses. El forecast era bueno, realmente tenía un nivel de exactitud bastante alto cuando se puso a prueba, sin embargo, el área de ventas me dijo que ellos necesitaban ver la información con mucho más detalle, es decir, ver un forecast por **cada producto que venden**. En ese momento pensé algo como _“Wow, la empresa tiene varios cientos de productos, esto me va a llevar una eternidad de realizar”_, por lo que comencé a plantearme algunas soluciones para minimizar el tiempo que invertiría en realizar ese forecast. Después de estar algunas horas pensando, probando y corrigiendo métodos, encontré uno que puede serte útil si te enfrentas a un problema similar.

#### [Mira la entrada completa aquí](https://bookdown.org/eljorgehdz/modelos_masivos/modelos-masivos.html "entrada")