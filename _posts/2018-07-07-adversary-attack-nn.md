---
layout: post
title: Adversary Attack NN
category: Machine Learning
---

En este post les mostrare como apartir de un modelo pre-entrenado de Redes Neuronales para Vision, en este caso de Google se puede confundir al mismo modelo para prediga objetos que no deberia, ha esto se le conoce como Ataque Adversario.

Entremos en materia, con Keras(Libreria de ML que corre sobre TensorFlow) descargamos el modelo pre-entrenado de InceptionV3 para vision computacional, el cual alberga en su interior yo diria que mas de 100 capas ocultas, y bien si tiene 100 capas en su interior es por que es capaz de predecir 1000 tipos de objetos con gran precision, ya luego de tener nuestro modelo previamente entrenado gracias a Keras, comenzamos a jugar con las capas de salida y entrada, para optimizar nuestra predicion, Hey pero queremos que aunque el modelo este bien y normalmente sepa que la imagen que le doy como input es un gato se equivoque, y como hacemos esto?, Ya lo he dicho previamente, Optimizacion, Como?

Esto es un poco mas de detalle, con las capas de entrada y salida, optimizaremos cual si fuese el modelo, pero lo que optimizaremos son los parametros(pixeles) de la imagen para que el modelo crea que es lo que nosotros queremos(En nuestro caso un limon), sin que sea visible para el ojo humano.

Heee esto esta denso y que tal si agregamos imagenes? Veamos que tal te va contra la IA

![Esto es un gato! ¡Awww!](/uploads/cat.jpg "Esto es un gato! ¡Awww!")

Esto es un gato? Claro esto es un gato y que tierno esta.

![](/uploads/hacked.png "LemonCat? Awww! WTF")

Quien diria el mismo gato? Pues no, esta vez no, segun la IA esta segunda imagen es un limon, Si se&ntilde;ores un limon! Sigue siendo tierno como limon.

Que no me crees? Mira los resultados

![](/uploads/screenshot-2018-07-06-google-colaboratory1.png)

Estos de arriba son los resultados de la prediccion del primer gatito, podemos ver que tiene una distribucion de probabilidades, las cuales se encabezan por tiger\_cat, tabby(raza de gato), egyptian\_cat, entre otros y aun asi el primer resultado no tiene gran probabilidad de ser, dado que hay mas categorias con las que coincide…

Ahora miremos el "Limon"

![](/uploads/screenshot-2018-07-06-google-colaboratory2.png)

Como vemos con la segunda imagen del gato, que frente a ojos humanos no ha sido alterada en lo mas minimo los resultados de su predicion han sido de un Limon! si un limon y con una probabilidad del 99.81% es practicamente un limon, y como ha sucedido esto?

Como te decia involucra capas de entrada y de salida del modelo y una optimizacion, la optimizacion en los parametros de la foto, al maximizar que la predicion se parezca a nuestro objetivo (limon), pero que no provoque tanta perturbacion en la imagen para que sea inperceptible para el ojo humano(minimizando la diferencia con la imagen original)

Ya! Quieres saber mas?

Vamos al codigo.

En esta [URL](https://colab.research.google.com/drive/1Zy5Lg1EicoVu-jcUBUZAkK8Phfp11p_k){: target="_blank"} esta todo, adelante, Diviertete

&nbsp;