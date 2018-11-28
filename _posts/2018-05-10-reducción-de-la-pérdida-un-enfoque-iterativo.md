---
layout: post
title: 'Reducción de la pérdida: Un enfoque iterativo'
category: Machine Learning
---

En el m&oacute;dulo anterior, se present&oacute; el concepto de p&eacute;rdida. Aqu&iacute;, aprender&aacute;s c&oacute;mo un modelo de aprendizaje autom&aacute;tico reduce la p&eacute;rdida de manera iterativa.

Es posible que el aprendizaje iterativo te recuerde el juego infantil en el que los objetos estaban fr&iacute;os o calientes (cerca o lejos) al intentar encontrar un elemento escondido, como un dedal. En este juego, el "objeto escondido" es el mejor modelo posible. Primero te arriesgar&aacute;s a adivinar ("El valor de W1 es 0".) y esperar&aacute;s a que el sistema te indique cu&aacute;l es la p&eacute;rdida. Luego, intentar&aacute;s adivinar otra vez ("El valor de W1 es 0.5".) y ver&aacute;s cu&aacute;l es la p&eacute;rdida. Bien, ya est&aacute;s m&aacute;s cerca. En realidad, si juegas a este juego correctamente, por lo general siempre estar&aacute;s m&aacute;s cerca. El verdadero truco del juego es intentar buscar el mejor modelo posible de la manera m&aacute;s eficaz posible.

La siguiente figura sugiere el proceso iterativo de prueba y error que usan los algoritmos de aprendizaje autom&aacute;tico para entrenar un modelo:

![](/uploads/screenshot-2018-5-10-reducción-de-la-pérdida-un-enfoque-iterativo-curso-intensivo-de-aprendizaje-automático-google-developers.png)

Figura 1. Un enfoque iterativo para entrenar un modelo.

Usaremos este mismo enfoque iterativo durante todo el Curso intensivo de aprendizaje autom&aacute;tico y detallaremos distintas complicaciones, particularmente dentro de la tormentosa nube azul. Las estrategias iterativas prevalecen en aprendizaje autom&aacute;tico, principalmente debido a que se ajustan muy bien a la escala de los conjuntos de datos de gran tama&ntilde;o.

El "modelo" toma uno o m&aacute;s atributos como entrada y devuelve una predicci&oacute;n (y') como resultado. Para simplificar, considera un modelo que toma un atributo y devuelve una predicci&oacute;n:

![](/uploads/screenshot-2018-5-10-reducción-de-la-pérdida-un-enfoque-iterativo-curso-intensivo-de-aprendizaje-automático-google-developers1.png)

&iquest;Qu&eacute; valores iniciales deber&iacute;amos establecer para B y W1? Para la regresi&oacute;n lineal, los valores de inicio no son importantes. Podr&iacute;amos elegir valores al azar, pero tomaremos los siguientes valores triviales en su lugar:

B = 0

W1 = 0

Sup&oacute;n que el primer valor del atributo es 10. Al vincular ese valor con el atributo de predicci&oacute;n, se obtiene lo siguiente:

&nbsp; y' = 0 + 0(10)<br>&nbsp; y' = 0

La parte de "C&aacute;lculo de p&eacute;rdida" del diagrama es la funci&oacute;n de p&eacute;rdida que usar&aacute; el modelo. Sup&oacute;n que usamos la funci&oacute;n de p&eacute;rdida al cuadrado. La funci&oacute;n de p&eacute;rdida incorpora dos valores de entrada:

y': la predicci&oacute;n del modelo para los atributos x

y: la etiqueta correcta correspondiente a los atributos x.

Finalmente, llegamos a la parte de "Actualizar par&aacute;metros" del diagrama. Aqu&iacute;, el sistema de aprendizaje autom&aacute;tico examina el valor de la funci&oacute;n de p&eacute;rdida y genera valores nuevos para B y W1. Por el momento, simplemente sup&oacute;n que el cuadro verde misterioso traza valores nuevos y, luego, el sistema de aprendizaje autom&aacute;tico vuelve a evaluar todos esos atributos con todas las etiquetas; se obtiene un nuevo valor para la funci&oacute;n de p&eacute;rdida, que genera valores de par&aacute;metros nuevos. El aprendizaje contin&uacute;a iterando hasta que el algoritmo descubre los par&aacute;metros del modelo con la p&eacute;rdida m&aacute;s baja posible. En general, iteras hasta que la p&eacute;rdida general deja de cambiar o, al menos, cambia muy lentamente. Cuando eso ocurre, decimos que el modelo ha **convergido**.

###### *Punto clave:*

###### *Un modelo de aprendizaje autom&aacute;tico se entrena comenzando con una hip&oacute;tesis inicial para los pesos y sesgo, y de manera iterativa ajustar esas hip&oacute;tesis hasta que se aprenden las ponderaciones y ordenadas al origen con la p&eacute;rdida m&aacute;s baja posible.*