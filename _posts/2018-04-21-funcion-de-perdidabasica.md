---
layout: post
title: Funcion de perdida(Basica)
category: Machine Learning
---

La p&eacute;rdida&nbsp;**L2**&nbsp;para un ejemplo determinado tambi&eacute;n se denomina **error al cuadrado.**

= Cuadrado de la diferencia entre la predicci&oacute;n y la etiqueta

= (observaci&oacute;n - predicci&oacute;n)2

= (y - y')2

Ya que queremos no solo reducir la p&eacute;rdida en un solo ejemplo, sino que nos interesa reducir la perdida en todo nuestro conjunto de datos:

<math xmlns="http://www.w3.org/1998/Math/MathML" display="block"> <semantics> <mrow> <mi>p</mi> <mrow class="MJX-TeXAtom-ORD"> <mo>&eacute;</mo> </mrow> <mi>r</mi> <mi>d</mi> <mi>i</mi> <mi>d</mi> <mi>a</mi> <mi>N</mi> <mn>2</mn> <mo>=</mo> <munder> <mo>&sum;<!--base32-c9gq6t9k68pk8xbechjpcubecnj3guhg5nh62wv56ct0-base32--></mo> <mrow class="MJX-TeXAtom-ORD"> <mo stretchy="false">(</mo> <mi>x</mi> <mo>,</mo> <mi>y</mi> <mo stretchy="false">)</mo> <mo>&isin;<!--base32-c9gq6t9k68pk8xbechjpcubecnj38chg5nh62wv56ct0-base32--></mo> <mi>D</mi> </mrow> </munder> <mo stretchy="false">(</mo> <mi>y</mi> <mo>&minus;<!--base32-c9gq6t9k68pk8xbechjpcubecnj3jchg5nh62wv56ct0-base32--></mo> <mi>p</mi> <mi>r</mi> <mi>e</mi> <mi>d</mi> <mi>i</mi> <mi>c</mi> <mi>c</mi> <mi>i</mi> <mrow class="MJX-TeXAtom-ORD"> <mo>&oacute;</mo> </mrow> <mi>n</mi> <mo stretchy="false">(</mo> <mi>x</mi> <mo stretchy="false">)</mo> <msup> <mo stretchy="false">)</mo> <mn>2</mn> </msup> </mrow> <annotation encoding="application/x-tex">p&eacute;rdida L2 = \sum_{(x,y)\in D} (y - predicci&oacute;n(x))^2</annotation> </semantics> </math>

&nbsp;

<math xmlns="http://www.w3.org/1998/Math/MathML"> <semantics> <mrow> <mo>&sum;<!--base32-c9gq6t9k68pk8xbechjpcubecnj3guhg5nh62wv56ct0-base32--></mo> <mtext>:Sumamos todos los ejemplos en el conjunto de entrenamiento.</mtext> </mrow> <annotation encoding="application/x-tex">\sum \text{:Sumamos todos los ejemplos en el conjunto de entrenamiento.}</annotation> </semantics> </math>
<br>
<math xmlns="http://www.w3.org/1998/Math/MathML"> <semantics> <mrow> <mi>D</mi> <mtext>: A veces es &uacute;til promediar todos los ejemplos,</mtext> </mrow> <annotation encoding="application/x-tex">D \text{: A veces es &uacute;til promediar todos los ejemplos}</annotation></semantics> </math>

<math xmlns="http://www.w3.org/1998/Math/MathML"> <semantics> <mrow> <mtext>entonces, hay que dividirlos por</mtext> <mfrac> <mn>1</mn> <mrow> <mo fence="false" stretchy="false">∥<!--base32-4undefinedjj0-base32--></mo> <mi>D</mi> <mo fence="false" stretchy="false">∥<!--base32-4undefinedjj0-base32--></mo> </mrow> </mfrac> <mo>.</mo> </mrow> <annotation encoding="application/x-tex">\text{entonces, hay que dividirlos por} \frac{1}{\|D\|}.</annotation> </semantics> </math>

&nbsp;
