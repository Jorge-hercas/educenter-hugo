+++
author = ""
bg_image = "/images/scholarship/scholarship-item-3.jpg"
categories = []
date = 2021-03-11T06:00:00Z
description = ""
draft = true
image = "/images/research/research-4.jpg"
tags = []
title = "markdown"
type = "post"

+++
\---

author: Jorge Hernández

categories:

\- R

date: "2021-02-22T00:00:00Z"

description: Este ejercicio tiene como objetivo aplicar de manera correcta el método SIMPLEX en R.

draft: false

tags:

\- Programación lineal

\- Maximización

\- Economía

title: Programación lineal. Método SIMPLEX en R.

type: post

\---

Dentro de la microeconomía, uno de los tópicos más usados en las empresas suele ser el de la *programación lineal*, ya que éstos métodos tienen como objetivo el analizar la forma de utilizar los recursos disponibles de la manera más **eficiente** posible, por ejemplo: Utilizar la menor cantidad de aluminio para crear una lata, obtener la mayor cantidad de beneficios posibles de una venta de productos, etc. Un método usado comunmente es el llamado **metodo SIMPLEX**, el cual se basa en iteraciones para poder obtener la combinación de recursos que *maximice* el beneficio, o bien, que *minimice* el costo, según sea el caso.

A partir de aquí vamos a partir de la idea de que el lector ya está familiarizado con los métodos de programación lineal, por lo que vamos a pasar directamente a dos ejercicios aplicados en R, para conocer la forma de hacerlo en este programa de manera práctica mediante el uso del paquete \`lpsolve\`.

\## Ejercicio 1.

La empresa “Arcoiris” produce pinturas para interiores y exteriores con dos materias primas, A y B. El siguiente cuadro resume las toneladas de materia prima que se requieren para cada tipo de pintura, la disponibilidad diaria de materia prima y la utilidad por tonelada para cada tipo de pintura:

\`\`\`{r echo=FALSE}

library(formattable)

Variables <- c("Materia prima A", "Materia prima B", "Utilidad por tonelada")

Exteriores <- c(6,1,5)

Interiores <- c(4,2,4)

\`Disponibilidad maxima diaria\` <- c(24,6, NA)

tabla1 <- data.frame(Variables, Exteriores, Interiores, \`Disponibilidad maxima diaria\`)

formattable(tabla1)

\`\`\`

Una encuesta de mercado indica que la demanda diaria de pintura para interiores no puede

exceder la de pintura para exteriores en más de una tonelada. Asimismo, que la demanda

diaria máxima de pintura para interiores es de dos toneladas. La empresa se propone

determinar la (mejor) combinación óptima de pinturas para interiores y exteriores que

maximice la utilidad diaria total. 

\**Solución:** La función objetivo es:

Sujeta a las restricciones:

El procedimiento para resolver el problema en R es el siguiente:

\`\`\`{r}

\# Cargamos el paquete necesario

library(lpSolve)

\# Matriz de la función objetivo

objetivo <- c(5,4)

\# Matriz de las restricciones 

restricciones <- matrix(c(6,4,

                          1,2,

                          1,-1,

                          0,1), nrow=4, byrow=TRUE)

\# Lado derecho de las restricciones 

derecho <- c(24, 6, 1, 2)

\# Dirección de las restricciones

direccion <- c("<=","<=","<=","<=")

\# Solución óptima 

optimo <- lp(direction = "max", 

   objective.in = objetivo,

   const.mat = restricciones,

   const.dir = direccion,

   const.rhs = derecho,

   all.int = T)

optimo

best_sol <- optimo$solution

names(best_sol) <- c("x_1", "x_2") 

print(best_sol)

\`\`\`

\## Ejercicio 2.

Laboratorios Novartis desea preparar un medicamento de tal manera que cada frasco contenga al menos 32 unidades de vitamina A, 10 de vitamina B y 40 de vitamina C. Para

suministrar estas vitaminas, el laboratorio emplea el aditivo X 1, a un costo de 2 dólares por onza, el cual contiene 15 unidades de vitamina A, 2 de B y 4 de C, un aditivo X 2 a un costo de 4 dólares por cada onza, que contiene 4 unidades de vitamina A, 2 de B y 14 de C. ¿Cuántas onzas de

cada aditivo se deben incluir en el frasco para minimizar el costo?

\**Solución:** La función objetivo es:

Sujeta a las restricciones:

El procedimiento en R es el siguiente:

\`\`\`{r}

\# Matriz de la función objetivo

objetivo1 <- c(2,4)

\# Matriz de las restricciones 

restricciones1 <- matrix(c(15,4,

                          2,2,

                          1,14), nrow=3, byrow=TRUE)

\# Lado derecho de las restricciones 

derecho1 <- c(32, 10, 40)

\# Dirección de las restricciones

direccion1 <- c(">=",">=",">=")

\# Solución óptima 

optimo1 <- lp(direction = "min", 

   objective.in = objetivo1,

   const.mat = restricciones1,

   const.dir = direccion1,

   const.rhs = derecho1,

   all.int = T)

optimo1

best_sol1 <- optimo1$solution

names(best_sol1) <- c("x_1", "x_2") 

print(best_sol1)

\`\`\`

\### \[Descarga el ejercicio en PDF\](/images/blog/ejercicios.pdf)

\## Referencias bibliográficas.

1\. Bazaraa, M. S., Jarvis, J. J., \\& Sherali, H. D. (1981). Programación lineal y flujo en redes (Vol. 2). Limusa.

2\. Hillier, F. S., \\& Lieberman, G. J. (2002). Investigación de operaciones. McGraw-Hill/Interamericana Editores, SA.

3\. Salas, H. G. (2009). Programación lineal aplicada. Ecoe Ediciones.

4\. Garrido, R. S. (1993). Programación Lineal, Metodología Y Problemas. Editorial Tebar.