---
layout: post
title: 'Reducción de la pérdida: Tasa de aprendizaje'
category: Machine Learning
---

Como se observ&oacute;, el vector de gradiente tiene una direcci&oacute;n y una magnitud. Los algoritmos de descenso de gradientes multiplican la gradiente por un escalar conocido como tasa de aprendizaje (o tama&ntilde;o del paso en algunas ocasiones) para determinar el siguiente punto. Por ejemplo, si la magnitud de la gradiente es 2.5 y la tasa de aprendizaje es 0.01, el algoritmo de descenso de gradientes tomar&aacute; el siguiente punto 0.025 m&aacute;s alejado del punto anterior.

Los hiperpar&aacute;metros son los controles que los programadores ajustan en los algoritmos de aprendizaje autom&aacute;tico. La mayor&iacute;a de los programadores de aprendizaje autom&aacute;tico pasan gran parte de su tiempo ajustando la tasa de aprendizaje. Si eliges una tasa de aprendizaje muy peque&ntilde;a, el aprendizaje llevar&aacute; demasiado tiempo:

![](/uploads/screenshot-2018-05-16-reducción-de-la-pérdida-tasa-de-aprendizaje-curso-intensivo-de-aprendizaje-automático-google-developers.png "Figura 6. La tasa de aprendizaje es muy pequeña.")

*Figura 6. La tasa de aprendizaje es muy peque&ntilde;a.*

A la inversa, si especificas una tasa de aprendizaje muy grande, el siguiente punto rebotar&aacute; al azar eternamente en la parte inferior, como un experimento de mec&aacute;nica cu&aacute;ntica que sali&oacute; muy mal:

![](/uploads/screenshot-2018-05-16-reducción-de-la-pérdida-tasa-de-aprendizaje-curso-intensivo-de-aprendizaje-automático-google-developers1.png "Figura 7. La tasa de aprendizaje es muy grande.")

*Figura 7. La tasa de aprendizaje es muy grande.*

Hay una tasa de aprendizaje con valor dorado para cada problema de regresi&oacute;n. El valor dorado est&aacute; relacionado con qu&eacute; tan plana es la funci&oacute;n de p&eacute;rdida. Si sabes que el gradiente de la funci&oacute;n de p&eacute;rdida es peque&ntilde;o, usa una tasa de aprendizaje mayor, que compensar&aacute; el gradiente peque&ntilde;o y dar&aacute; como resultado un tama&ntilde;o del paso m&aacute;s grande.

![](/uploads/screenshot-2018-05-16-reducción-de-la-pérdida-tasa-de-aprendizaje-curso-intensivo-de-aprendizaje-automático-google-developers2.png "Figura 8. La tasa de aprendizaje es la correcta.")

*Figura 8. La tasa de aprendizaje es la correcta.*