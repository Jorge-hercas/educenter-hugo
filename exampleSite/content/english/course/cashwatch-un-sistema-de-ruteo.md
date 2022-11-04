+++
apply_url = "jorgehcas1998.shinyapps.io/CashWach/"
bg_image = "/images/net.jpg"
category = "Estadística"
date = 2022-11-04T06:00:00Z
description = "App creada para llevar al usuario a su cajero más cercano"
duration = ""
fee = ""
image = "/images/captura-de-pantalla-2022-11-04-a-la-s-10-27-28.png"
teacher = "Jorge Hernández"
title = "CashWatch: Un sistema de ruteo"
weekly = ""

+++
## **CashWatch**

Una aplicación dedicada a los usuarios de BBVA, con la cual podrás conocer el estatus de tu cajero más cercano, así como una ruta para llegar a tu mejor opción (en el mejor horario posible).

La idea detrás de CashWatch es proporcionarle los usuarios una solución rápida y accesible para consultar información sobre cajeros automáticos a través de una aplicación web. CashWatch será capaz de ofrecer al usuario información georeferenciada en tiempo real sobre los cajeros automáticos en un área determinada, como: concentración territorial de cajeros (heatmap), estatus de los cajeros (información sobre fallas), pronóstico de fallas por cajero ('score' de riesgo) y, finalmente, calcular una ruta para el usuario hacia el cajero más cercano usando la API de Google Maps. Todo esto, con el objetivo de proveer al usuario con la mejor y más completa información para que este pueda planear con anticipación su visita a un cajero; así como otorgarle al negocio información suficiente para poder optimizar tanto el funcionamiento como la distribución espacial de los cajeros.

CashWatch es una aplicación web interactiva optimizada tanto para dispositivos móviles como para equipo de cómputo. Esta funciona sobre tres lenguajes principalmente: JavaScript, HTML y R. La interfaz de la aplicación usa Mapbox para generar una plantilla del mapa de México sobre la cual se visualiza la ubicación de cada ATM. Esta interfaz se alimenta de dos APIs: la de Mapbox para el shapefile y la de Google Maps para el input del usuario. De esta forma, el usuario podrá proporcionar a la aplicación una ubicación específica (o tomar automáticamente su ubicación actual) y esta calculará la ruta óptima al ATM más cercano, considerando la probabilidad de fallo de los ATM. Al hacer esto, también se desplegará información visual sobre el cajero seleccionado (estatus y pronóstico de falla) en ventanas flotantes con la librería Apache ECharts.

Creadores de la app: Jorge Hernandez, Eugenio Mora, Sebastian Ocampo y Diego Lopez

#### [Mira la app aquí](jorgehcas1998.shinyapps.io/CashWach/ "xd")

#### [Repositorio de Github](https://github.com/Jorge-hercas/CashWatch "repo")