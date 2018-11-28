---
layout: post
title: Regresión lineal
category: Machine Learning
---

Es sabido que los grillos cantan con m&aacute;s frecuencias en los d&iacute;as de m&aacute;s calor. Durante d&eacute;cadas, entom&oacute;logos profesionales y aficionados han catalogado datos sobre la cantidad de cantos por minuto y la temperatura. Para tu cumplea&ntilde;os, la t&iacute;a Ruth te regal&oacute; su amada base de datos sobre grillos y te invita a que aprendas un modelo para predecir dicha relaci&oacute;n.
{: .present-before-paste}

En primer lugar, es necesario realizar una representaci&oacute;n de los datos para examinarlos:
{: .present-before-paste}

![](/uploads/screenshot-2018-5-10-estudio-detallado-del-aa-regresión-lineal-curso-intensivo-de-aprendizaje-automático-google-developers.png)
{: .present-before-paste}

Figura 1. Cantos por minuto contra temperatura
{: .present-before-paste}

Efectivamente, la representaci&oacute;n muestra que la cantidad de cantos aumenta con la temperatura. &iquest;Es lineal la relaci&oacute;n entre los cantos y la temperatura? S&iacute;, ya que es posible dibujar una l&iacute;nea recta como la siguiente para representar dicha relaci&oacute;n:
{: .present-before-paste}

![](/uploads/screenshot-2018-5-10-estudio-detallado-del-aa-regresión-lineal-curso-intensivo-de-aprendizaje-automático-google-developers1.png)
{: .present-before-paste}

Figura 2. Una relaci&oacute;n lineal
{: .present-before-paste}

Si bien la l&iacute;nea no pasa perfectamente por cada punto, demuestra con claridad la relaci&oacute;n entre la temperatura y los cantos por minuto para dichos puntos. Si aplicamos un poco de &aacute;lgebra, podemos determinar esta relaci&oacute;n de la siguiente manera:
{: .present-before-paste}

***y=mx+b***
{: .present-before-paste}

donde:
{: .present-before-paste}

**y** es la temperatura en grados cent&iacute;grados, correspondiente al valor que intentamos predecir.
{: .present-before-paste}

**m** es la pendiente de la l&iacute;nea.
{: .present-before-paste}

**x** es la cantidad de cantos por minuto, correspondiente al valor de nuestro atributo de entrada.
{: .present-before-paste}

**b** es la intersecci&oacute;n en y.
{: .present-before-paste}

Seg&uacute;n las convenciones del aprendizaje autom&aacute;tico, la ecuaci&oacute;n para un modelo se escribir&aacute; de una forma un poco diferente:
{: .present-before-paste}

**y′=b+w1x1**
{: .present-before-paste}

donde:
{: .present-before-paste}

**y′** es la etiqueta predicha (un resultado deseado).
{: .present-before-paste}

**b** es la ordenada al origen (la intersecci&oacute;n en y). En alguna literatura de aprendizaje autom&aacute;tico, se hace referencia a ella como w0.
{: .present-before-paste}

**w1** es la ponderaci&oacute;n del atributo 1. La ponderaci&oacute;n es el mismo concepto de la "pendiente" m, que se indic&oacute; anteriormente.
{: .present-before-paste}

**x1** es un atributo (una entrada conocida).
{: .present-before-paste}

Para inferir (predecir) la temperatura y′ para un valor nuevo de cantos por minuto x1, solo agrega el valor de x1 a este modelo.
{: .present-before-paste}

Los sub&iacute;ndices (p. ej., w1 y x1) indican modelos m&aacute;s sofisticados que se basan en varios atributos. Por ejemplo, un modelo que se basa en tres atributos usar&iacute;a la siguiente ecuaci&oacute;n:
{: .present-before-paste}

***y′=b+w1x1+w2x2+w3x3***
{: .present-before-paste}