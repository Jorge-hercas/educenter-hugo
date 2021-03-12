+++
author = "Jorge Hernández Castelán"
bg_image = "/images/net.jpg"
categories = ["R"]
date = 2021-01-12T06:00:00Z
description = "Este ejercicio tiene como objetivo crear gráficos con una tendencia ciclo a partir de su estacionalidad"
image = "/images/rlogo.png"
tags = ["Estacionalidad", "Gráficos", "Series de tiempo"]
title = "Gráficos desestacionalizados interactivos en R"
type = "post"

+++
## Entendiendo la estacionalidad

Las series de tiempo son una clase de datos que están estructuradon en el tiempo (valga la redundancia), es decir, cada observación se refiere a un periodo en particular y estas tienden a ser menos volátiles que los datos de corte transversal. Estas suelen tener ciertos componentes que las caracterizan, como son:

1. Tendencia: La tendencia puede definirse como la trayectoría que sigue la serie de tiempo en el largo plazo, o el cambio en la media, la cual suele ser un movimiento suave de la serie a largo plazo.
2. Componente estacional: Las series de tiempo en el corto plazo suelen tener un componente denominado estacional, el cual hará que incrementen o disminuyan según el periodo de tiempo sin cambiar su tendencia de largo plazo. Por ejemplo, supongamos las ventas de una empresa de juguetes. Estas tenderan a un cierto nivel durante la mayoría del año, pero en diciembre y épocas navideñas tenderán a incrementar.
3. Componente aleatorio: Este componente (conocido también como “Random Walk” o caminata aleatoria, aunque este nombre suele ser usado para series de tiempo sin tendencia o componente estacional, como el precio de las acciones de una compañía) es algo que no puede ser predecido por medio de modelos de series de tiempo, ya que son eventos fortuitos que ocurren de manera sorpresiva, como un desastre natural, una pandemia, etc.

### [Mira el ejercicio completo aquí](https://bookdown.org/eljorgehdz/desestascionalizado/ "graficos")