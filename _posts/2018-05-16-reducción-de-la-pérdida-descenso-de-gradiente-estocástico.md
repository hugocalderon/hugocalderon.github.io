---
layout: post
title: 'Reducción de la pérdida: Descenso de gradiente estocástico'
category: Machine Learning
---

En el descenso de gradientes, un lote es la cantidad total de ejemplos que usas para calcular la gradiente en una sola iteraci&oacute;n. Hasta ahora, hemos supuesto que el lote era el conjunto de datos completo. Al trabajar a la escala de Google, los conjuntos de datos suelen tener miles de millones o incluso cientos de miles de millones de ejemplos. Adem&aacute;s, los conjuntos de datos de Google con frecuencia contienen inmensas cantidades de atributos. En consecuencia, un lote puede ser enorme. Un lote muy grande puede causar que incluso una sola iteraci&oacute;n tome un tiempo muy prolongado para calcularse.

Es probable que un conjunto de datos grande con ejemplos muestreados al azar contenga datos redundantes. De hecho, la redundancia se vuelve m&aacute;s probable a medida que aumenta el tama&ntilde;o del lote. Un poco de redundancia puede ser &uacute;til para atenuar las gradientes inconsistentes, pero los lotes enormes tienden a no tener un valor mucho m&aacute;s predictivo que los lotes grandes.

&iquest;C&oacute;mo ser&iacute;a si pudi&eacute;ramos obtener la gradiente correcta en promedio con mucho menos c&oacute;mputo? Al elegir ejemplos al azar de nuestro conjunto de datos, podr&iacute;amos estimar (si bien de manera inconsistente) un promedio grande de otro mucho m&aacute;s peque&ntilde;o. El descenso de gradiente estoc&aacute;stico (SGD) lleva esta idea al extremo: usa un solo ejemplo (un tama&ntilde;o del lote de 1) por iteraci&oacute;n. Cuando se dan demasiadas iteraciones, el SGD funciona, pero es muy inconsistente. El t&eacute;rmino "estoc&aacute;stico" indica que el ejemplo &uacute;nico que compone cada lote se elige al azar.

El descenso de gradiente estoc&aacute;stico de minilote (SGD de minilote) es un equilibrio entre la iteraci&oacute;n de lote completo y el SGD. Un minilote generalmente tiene entre 10 y 1,000 ejemplos, elegidos al azar. El SGD de minilote reduce la cantidad de inconsistencia en el SGD, pero sigue siendo m&aacute;s eficaz que el lote completo.

Para simplificar la explicaci&oacute;n, nos concentramos en el descenso de gradientes para un solo atributo. Te garantizamos que el descenso de gradientes tambi&eacute;n funciona en conjuntos de varios atributos.