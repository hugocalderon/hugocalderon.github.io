---
layout: post
title: 'Reducción de la pérdida: Descenso de gradientes'
category: Machine Learning
---

[El diagrama de enfoque iterativo](https://willarevalo.github.io/machine%20learning/2018/05/10/reducci%C3%B3n-de-la-p%C3%A9rdida-un-enfoque-iterativo.html)&nbsp;conten&iacute;a un cuadro verde con afirmaciones sin fundamento llamado "Actualizar par&aacute;metros". Ahora reemplazaremos esa soluci&oacute;n algor&iacute;tmica m&aacute;gica por algo m&aacute;s sustancial.

Sup&oacute;n que tuvi&eacute;ramos el tiempo y los recursos de c&oacute;mputo para calcular la p&eacute;rdida de todos los valores posibles de w1. Para el tipo de problemas de regresi&oacute;n que hemos estado examinando, la representaci&oacute;n resultante de p&eacute;rdida frente a w1 siempre ser&aacute; convexa. En otras palabras, la representaci&oacute;n siempre tendr&aacute; forma de taz&oacute;n, como la siguiente:

![](/uploads/screenshot-2018-05-16-reducción-de-la-pérdida-descenso-de-gradientes-curso-intensivo-de-aprendizaje-automático-google-devel---.png "Figura 2. Los problemas de regresión producen gráficas de pérdida convexa vs. pesos.")

*Figura 2. Los problemas de regresi&oacute;n producen gr&aacute;ficas de p&eacute;rdida convexa vs. pesos.*

&nbsp;

Los problemas convexos tienen un solo m&iacute;nimo, es decir, un solo lugar en el que la pendiente es exactamente 0. Ese m&iacute;nimo es donde converge la funci&oacute;n de p&eacute;rdida.

Calcular la funci&oacute;n de p&eacute;rdida para cada valor concebible de W1 en todo el conjunto de datos ser&iacute;a una manera ineficaz de buscar el punto de convergencia. Examinemos un mecanismo m&aacute;s &uacute;til, muy popular en el aprendizaje autom&aacute;tico, denominado descenso de gradientes.

La primera etapa en el descenso de gradientes es elegir un valor de inicio (un punto de partida) para W1. El punto de partida no es muy importante; por lo tanto, muchos algoritmos simplemente establecen W1 en 0 o eligen un valor al azar. En la siguiente figura, se muestra que elegimos un punto de partida levemente mayor que 0.

![](/uploads/screenshot-2018-05-16-reducción-de-la-pérdida-descenso-de-gradientes-curso-intensivo-de-aprendizaje-automático-google-devel---1.png "Figura 3. Un punto de partida para el descenso de gradientes.")

*Figura 3. Un punto de partida para el descenso de gradientes.*

Luego, el algoritmo de descenso de gradientes calcula la gradiente de la curva de p&eacute;rdida en el punto de partida. En resumen, una **gradiente** es un vector de derivadas parciales; indica por d&oacute;nde es m&aacute;s cerca o m&aacute;s lejos. Ten en cuenta que la gradiente de p&eacute;rdida con respecto a un solo peso (como en la Figura 3) es equivalente a la derivada.

Ten en cuenta que la gradiente es un vector, de manera que tiene las dos caracter&iacute;sticas siguientes:

* una direcci&oacute;n
* una magnitud

La gradiente siempre apunta en la direcci&oacute;n del aumento m&aacute;s empinado de la funci&oacute;n de p&eacute;rdida. El algoritmo de descenso de gradientes toma un paso en direcci&oacute;n de la gradiente negativa para reducir la p&eacute;rdida lo m&aacute;s r&aacute;pido posible.

![](/uploads/screenshot-2018-05-16-reducción-de-la-pérdida-descenso-de-gradientes-curso-intensivo-de-aprendizaje-automático-google-devel---2.png "Figura 4. El descenso de gradientes se basa en gradientes negativas.")

*Figura 4. El descenso de gradientes se basa en gradientes negativas.*

Para determinar el siguiente punto a lo largo de la curva de la funci&oacute;n de p&eacute;rdida, el algoritmo de descenso de gradientes agrega alguna fracci&oacute;n de la magnitud de la gradiente al punto de partida, como se muestra en la siguiente figura:

![](/uploads/screenshot-2018-05-16-reducción-de-la-pérdida-descenso-de-gradientes-curso-intensivo-de-aprendizaje-automático-google-devel---3.png "Figura 5. Un paso de la gradiente nos mueve hacia el siguiente punto en la curva de pérdida.")

*Figura 5. Un paso de la gradiente nos mueve hacia el siguiente punto en la curva de p&eacute;rdida.*

Luego, el descenso de gradientes repite este proceso y se acerca cada vez m&aacute;s al m&iacute;nimo.