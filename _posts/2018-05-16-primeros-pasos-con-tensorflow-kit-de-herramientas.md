---
layout: post
title: 'Primeros pasos con TensorFlow: Kit de herramientas'
category: Machine Learning
---

En la siguiente figura, se muestra la jerarqu&iacute;a actual de los kits de herramientas de TensorFlow:

![](/uploads/screenshot-2018-05-16-primeros-pasos-con-tensorflow-kit-de-herramientas-curso-intensivo-de-aprendizaje-automático-google-de---.png)

*Figura 1. Jerarqu&iacute;a de los kits de herramientas de TensorFlow.*

En la siguiente tabla, se resumen los objetivos de las diferentes capas:

![](/uploads/screenshot-2018-05-16-primeros-pasos-con-tensorflow-kit-de-herramientas-curso-intensivo-de-aprendizaje-automático-google-de---1.png)

TensorFlow consiste en los siguientes dos componentes:

* un b&uacute;fer de protocolos de gr&aacute;ficos
* un tiempo de ejecuci&oacute;n que ejecuta el gr&aacute;fico (distribuido)

Estos dos componentes son an&aacute;logos al compilador de Java y a la JVM. Cuando la JVM se implementa en varias plataformas de hardware, tambi&eacute;n lo hace TensorFlow (CPU y GPU).

&iquest;Qu&eacute; API debes usar? Debes usar el nivel de abstracci&oacute;n m&aacute;s alto que resuelva el problema. Los niveles de abstracci&oacute;n m&aacute;s altos son m&aacute;s f&aacute;ciles de usar, pero tambi&eacute;n son menos flexibles (por su dise&ntilde;o). Te recomendamos comenzar con la API de nivel m&aacute;s alto y poner todo en funcionamiento. Si necesitas flexibilidad adicional por cuestiones de modelos especiales, usa un nivel m&aacute;s bajo. Ten en cuenta que cada nivel se crea con API de niveles inferiores, por lo que la reducci&oacute;n de jerarqu&iacute;a deber&iacute;a ser razonablemente directa.

&nbsp;