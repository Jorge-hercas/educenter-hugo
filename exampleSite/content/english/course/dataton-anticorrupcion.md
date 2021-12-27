+++
apply_url = "https://jorgehcas1998.shinyapps.io/Dataton-corrupcion/"
bg_image = "/images/net.jpg"
category = "Estadística descriptiva"
date = 2021-12-27T06:00:00Z
description = "Aplicación destinada a reconocer casos atípicos de corrupción en México"
duration = ""
fee = ""
image = "/images/captura-de-pantalla-2021-12-27-a-la-s-15-24-33.png"
teacher = "Jorge Hernández"
title = "DATATON: Anticorrupción"
weekly = ""

+++
## Un vistazo a la corrupción

En los últimos años se ha hecho hincapié en lo dañino que puede ser la corrupción en el país, así como los efectos que ésta puede tener, por lo que se han hecho esfuerzos para poder detectarla y erradicarla, pero ¿cómo se puede contribuir a esto? Una forma analítica de hacerlo es mediante una aplicación en Shiny que permita visualizar (mediante una cierta metodología) aquellos casos que se puedan tomar como "_posible corrupción_". 

Si bien los casos atípicos pueden ser un poco ambiguos de detectar, se optó por utilizar un método sencillo para averiguar cuales son los posibles casos de corrupción para funcionarios de la CDMX. La idea es sencilla: Un gráfico de estilo **"boxplot"** nos muestra aquellos datos que se encuentran dentro de una media y un cierto rango, pero aquellos puntos fuera de dicho rango serán catalogados como **outliers**, o bien, datos atípicos, por lo que utilizando la función respectiva en R y extrayendo los datos del boxplot considerados como outliers, podemos identificarlos rápidamente.

### [Mira la aplicación justo aquí](https://jorgehcas1998.shinyapps.io/Dataton-corrupcion/ "app")