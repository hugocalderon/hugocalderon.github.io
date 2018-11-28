---
layout: post
title: Como reducir la perdida
category: Machine Learning
---

&iquest;C&oacute;mo se reduce la p&eacute;rdida?

La derivada de (y - y')2 con respecto a los pesos y sesgos nos indica c&oacute;mo cambia la p&eacute;rdida en un ejemplo determinado:

Es simple de computar y convexa.

Por lo tanto, tomamos pasos peque&ntilde;os reiteradamente en la direcci&oacute;n que minimiza la p&eacute;rdida:

Los llamamos pasos de gradiente (aunque en realidad son pasos de gradiente negativos).

Esta estrategia de optimizaci&oacute;n se denomina descenso de gradientes.

Ejercicios que te ayudaran a contextualizar mas la perdida y como reducirla [AQU&Iacute;](https://developers.google.com/machine-learning/crash-course/fitter/graph)

##### Inicializacion de pesos

![](/uploads/screenshot-2018-5-10-reducción-de-la-pérdida-curso-intensivo-de-aprendizaje-automático-google-developers.png)

##### SGD y descenso de gradientes de minilote

La gradiente se podr&iacute;a calcular en todo el conjunto de datos en cada paso, pero esto es innecesario:

El c&aacute;lculo de la gradiente en peque&ntilde;as muestras de datos funciona bien.

En cada paso, se debe obtener una nueva muestra al azar.

**Descenso de gradiente estoc&aacute;stico**: Se toma un ejemplo por vez.

**Descenso de gradientes de minilote**: Se usan lotes de 10 a 1000.

La p&eacute;rdida y las gradientes se promedian en el lote.