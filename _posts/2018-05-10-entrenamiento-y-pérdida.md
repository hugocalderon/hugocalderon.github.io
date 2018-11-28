---
layout: post
title: Entrenamiento y pérdida
category: Machine Learning
---

**Entrenar** un modelo simplemente significa aprender (determinar) valores correctos para todas las ponderaciones y las ordenadas al origen de los ejemplos etiquetados. En un aprendizaje supervisado, el algoritmo de un aprendizaje autom&aacute;tico construye un modelo al examinar varios ejemplos e intentar encontrar un modelo que minimice la p&eacute;rdida. Este proceso se denomina **minimizaci&oacute;n del riesgo emp&iacute;rico.**

La p&eacute;rdida es una penalidad por una predicci&oacute;n incorrecta. Esto quiere decir que la **p&eacute;rdida** es un n&uacute;mero que indica qu&eacute; tan incorrecta fue la predicci&oacute;n del modelo en un solo ejemplo. Si la predicci&oacute;n del modelo es perfecta, la p&eacute;rdida es cero; de lo contrario, la p&eacute;rdida es mayor. El objetivo de entrenar un modelo es encontrar un conjunto de ponderaciones y ordenadas al origen que, en promedio, tengan p&eacute;rdidas bajas en todos los ejemplos. Por ejemplo, la Figura 3 muestra un modelo al lado izquierdo con una p&eacute;rdida alta, y al lado derecho un modelo con p&eacute;rdida baja. Ten en cuenta lo siguiente con respecto a la imagen:

* La flecha roja representa la p&eacute;rdida.
* La l&iacute;nea azul representa las predicciones.

![](/uploads/screenshot-2018-5-10-estudio-detallado-del-aa-entrenamiento-y-pérdida-curso-intensivo-de-aprendizaje-automático-google-deve---.png)

Figura 3. P&eacute;rdida alta en el modelo de la izquierda; p&eacute;rdida baja en el modelo de la derecha.

Ten en cuenta que las flechas rojas en la figura izquierda son mucho m&aacute;s largas que las de la figura derecha. Claramente, la flecha azul en la figura de la derecha es un modelo de predicci&oacute;n mucho m&aacute;s acertado que la flecha azul en la figura de la izquierda.

Tal vez te preguntes si puedes crear una funci&oacute;n matem&aacute;tica (una funci&oacute;n de p&eacute;rdida) que sume las p&eacute;rdidas individuales de una forma que tenga sentido.

##### P&eacute;rdida al cuadrado: Una funci&oacute;n popular de p&eacute;rdida

Los modelos de regresi&oacute;n lineal que se examinan aqu&iacute; usan una funci&oacute;n de p&eacute;rdida llamada **p&eacute;rdida al cuadrado**(tambi&eacute;n conocida como p&eacute;rdida **L2**). A continuaci&oacute;n, se muestra la p&eacute;rdida al cuadrado para un &uacute;nico ejemplo:

```
  = the square of the difference between the label and the prediction
  = (observation - prediction(x))2
  = (y - y')2
```

El **error cuadr&aacute;tico medio (ECM)** es el promedio de la p&eacute;rdida al cuadrado de cada ejemplo. Para calcular el ECM, sumamos todas las p&eacute;rdidas al cuadrado de los ejemplos individuales y, luego, lo dividimos por la cantidad de ejemplos:

![](/uploads/screenshot-2018-5-10-estudio-detallado-del-aa-entrenamiento-y-pérdida-curso-intensivo-de-aprendizaje-automático-google-deve---1.png)

donde:

* (x,y) es un ejemplo en el que
* x es el conjunto de atributos (p. ej., temperatura, edad y &eacute;xito para aparearse) que el modelo usa para realizar las predicciones.
* y es la etiqueta del ejemplo (p. ej., cantos por minuto).
* prediction(x) es un atributo de las ponderaciones y las ordenadas al origen en combinaci&oacute;n con el conjunto de atributos x.
* D es el conjunto de datos que contiene muchos ejemplos etiquetados, que son los pares (x,y).
* N es la cantidad de ejemplos en D.

Si bien MSE se usa com&uacute;nmente en el aprendizaje autom&aacute;tico, no es la &uacute;nica funci&oacute;n de p&eacute;rdida pr&aacute;ctica ni la mejor para todas las circunstancias.