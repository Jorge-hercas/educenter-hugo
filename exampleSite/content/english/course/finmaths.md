+++
apply_url = "https://github.com/Jorge-hercas/FinMaths"
bg_image = "/images/net.jpg"
category = "r package"
date = 2022-07-12T05:00:00Z
description = "Introducción a mi nueva librería de matemáticas financieras: FinMaths"
duration = ""
fee = ""
image = "/images/logo_small.png"
teacher = "Jorge Hernández"
title = ""
weekly = ""

+++
## FinMaths

La finalidad de este paquete es poder simplificar en la medida de lo posible los cálculos realizados para las áreas financieras, poder generarlos en masa y aumentar la eficiencia de éstos.

[Puedes descargarlo en ésta liga.](https://github.com/Jorge-hercas/FinMaths "XS")

O mediante la siguiente línea de códigos:

    devtools::install_github("Jorge-hercas/FinMaths") 

Uso básico del paquete:

    library(FinMaths)
    library(dplyr)
    tibble(
      capital = sample(100:200,20,replace = TRUE),
      tiempo = sample(1:24,20,replace = TRUE),
      interes = sample((1:8)/32,20,replace = TRUE),
      periodicidad = sample(1:365,20,replace = TRUE)
    ) |> 
      mutate(
        inversion_tasa_simple = valor_futuro_simple(capital,tiempo,interes,periodicidad),
        inversion_tasa_comp = valor_futuro_compuesto(capital,tiempo,interes,periodicidad)
      )
    
    # A tibble: 20 x 5
       capital tiempo interes periodicidad inversion_tasa_simple                            
         <int>  <int>   <dbl>        <int> <chr>                                            
     1     181      9  0.219            72 El valor futuro con tu inversión será de $185.949
     2     149     20  0.125           254 El valor futuro con tu inversión será de $150.467
     3     110      6  0.0938           69 El valor futuro con tu inversión será de $110.897
     4     135     14  0.188            83 El valor futuro con tu inversión será de $139.27 
     5     171     24  0.0625          282 El valor futuro con tu inversión será de $171.91 
     6     124     22  0.219           198 El valor futuro con tu inversión será de $127.014
     7     156      4  0.0312          319 El valor futuro con tu inversión será de $156.061
     8     107     13  0.0312          244 El valor futuro con tu inversión será de $107.178
     9     189      7  0.0625          105 El valor futuro con tu inversión será de $189.787
    10     151      2  0.0938          259 El valor futuro con tu inversión será de $151.109
    11     195     12  0.0312          257 El valor futuro con tu inversión será de $195.285
    12     164     21  0.0938          261 El valor futuro con tu inversión será de $165.237
    13     118     21  0.156            82 El valor futuro con tu inversión será de $122.722
    14     187     12  0.156           120 El valor futuro con tu inversión será de $189.922
    15     110      2  0.0625           18 El valor futuro con tu inversión será de $110.764
    16     164      9  0.125           118 El valor futuro con tu inversión será de $165.564
    17     101     22  0.219           345 El valor futuro con tu inversión será de $102.409
    18     164     15  0.188           245 El valor futuro con tu inversión será de $165.883
    19     179     17  0.219           233 El valor futuro con tu inversión será de $181.857
    20     155      7  0.219           223 El valor futuro con tu inversión será de $156.064