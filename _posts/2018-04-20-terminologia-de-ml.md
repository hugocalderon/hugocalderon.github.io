---
layout: post
title: Terminologia de ML
category: Machine Learning
---

Si quieres comenzar en el grandioso mundo del Machine Learning o aprendizaje autom&aacute;tico debes tener muy en cuenta estos t&eacute;rminos que se utilizan en el campo.

Estos terminos estan dados por google en su curso de AA(Apredizaje Automatico) que dejare en este [link](https://developers.google.com/machine-learning/crash-course/framing/ml-terminology) para quien interese, sin mas esta es la terminologia:

&iquest;Qu&eacute; es el aprendizaje autom&aacute;tico (supervisado)? A continuaci&oacute;n, se incluye una definici&oacute;n concisa:

* Los sistemas de AA aprenden c&oacute;mo combinar entradas para producir predicciones &uacute;tiles sobre datos nunca antes vistos.

Exploremos la terminolog&iacute;a b&aacute;sica del aprendizaje autom&aacute;tico.

## Etiquetas

Una&nbsp;**etiqueta**&nbsp;es el valor que estamos prediciendo, es decir, la variable y en la regresi&oacute;n lineal simple. La etiqueta podr&iacute;a ser el precio futuro del trigo, el tipo de animal que se muestra en una imagen, el significado de un clip de audio o simplemente cualquier cosa.

## Atributos

Un&nbsp;**atributo**&nbsp;es una variable de entrada, es decir, la variable x en la regresi&oacute;n lineal simple. Un proyecto de aprendizaje autom&aacute;tico simple podr&iacute;a usar un solo atributo, mientras que otro m&aacute;s sofisticado podr&iacute;a usar millones de atributos, especificados como:

*{x1,x2,…x<sub>N</sub>}*

En el ejemplo del detector de spam, los atributos podr&iacute;an incluir los siguientes:

* palabras en el texto del correo electr&oacute;nico
* direcci&oacute;n del remitente
* hora del d&iacute;a a la que se envi&oacute;
* presencia de la frase "un truco incre&iacute;ble" en el correo electr&oacute;nico

## Ejemplos

Un ejemplo es una instancia de datos en particular, **x**. (La **x**&nbsp;se coloca en negrita para indicar que es un vector). Los ejemplos se dividen en dos categor&iacute;as:

* ejemplos etiquetados
* ejemplos sin etiqueta

Un **ejemplo etiquetado** incluye tanto atributos como la etiqueta. Esto significa lo siguiente:

&nbsp; `labeled examples: {features, label}: (x, y)`

Los ejemplos etiquetados se usan para&nbsp;**entrenar**&nbsp;el modelo. En nuestro ejemplo del detector de spam, los ejemplos etiquetados ser&iacute;an los correos electr&oacute;nicos individuales que los usuarios marcaron expl&iacute;citamente como "es spam" o "no es spam".

Por ejemplo, en la siguiente tabla se muestran 5 ejemplos etiquetados de un conjunto de datos que contiene informaci&oacute;n sobre los precios de vivienda en California:

<img class="u-full-width" src="/uploads/screenshot-2018-4-19-framing-key-ml-terminology-machine-learning-crash-course-google-developers.png" alt="">

Un**&nbsp;ejemplo sin etiqueta**&nbsp;contiene atributos, pero no la etiqueta. Esto significa lo siguiente:

&nbsp; `unlabeled examples: {features, ?}: (x, ?)`

Una vez que el modelo se entrena con ejemplos etiquetados, ese modelo se usa para predecir la etiqueta en ejemplos sin etiqueta. En el detector de spam, los ejemplos sin etiqueta son correos electr&oacute;nicos nuevos que las personas todav&iacute;a no han etiquetado.

## Modelos

Un modelo define la relaci&oacute;n entre los atributos y la etiqueta. Por ejemplo, un modelo de detecci&oacute;n de spam podr&iacute;a asociar de manera muy definida determinados atributos con "es spam". Destaquemos dos fases en el ciclo de un modelo:

* **Entrenamiento**&nbsp;significa crear o aprender el modelo. Es decir, le muestras ejemplos etiquetados al modelo y permites que este aprenda gradualmente las relaciones entre los atributos y la etiqueta.
* **Inferencia**&nbsp;significa aplicar el modelo entrenado a ejemplos sin etiqueta. Es decir, usas el modelo entrenado para realizar predicciones &uacute;tiles (`y'`). Por ejemplo, durante la inferencia, puedes predecir `medianHouseValue` para nuevos ejemplos sin etiqueta.

## Regresi&oacute;n frente a clasificaci&oacute;n

Un modelo de&nbsp;**regresi&oacute;n**&nbsp;predice valores continuos. Por ejemplo, los modelos de regresi&oacute;n hacen predicciones que responden a preguntas como las siguientes:

* &iquest;Cu&aacute;l es el valor de una casa en California?
* &iquest;Cu&aacute;l es la probabilidad de que un usuario haga clic en este anuncio?

Un modelo de&nbsp;**clasificaci&oacute;n**&nbsp;predice valores discretos. Por ejemplo, los modelos de clasificaci&oacute;n hacen predicciones que responden a preguntas como las siguientes:

* &iquest;Un mensaje de correo electr&oacute;nico determinado es spam o no es spam?
* &iquest;Esta imagen es de un perro, un gato o un h&aacute;mster?