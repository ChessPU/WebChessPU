---
layout: post
title: Múltiples leds con Arduino
permalink: /blog/:day-:month-:year/multiples-leds-con-arduino
location: Mora de Rubielos
---
Las intensas nevadas del fin de semana pasado han dado paso a unos días de 
mucho hielo y, aunque ya se puede circular en coche, solo hemos hecho una breve
visita a Virgen de la Vega. Los establecimientos cerrados y las nuevas 
restricciones que entraron hoy en vigor a las 00:00, no dan muchas opciones en
días de frío. Un pequeño paseo y hemos vuelto

{% assign img_url = "/assets/img/personal/virgen-de-la-vega-1-16-01-2021-2.jpeg" %}
{% assign img_description = "Mi querida Dana contemplando la nieve" %}
{% include blog/one-image.html %}

Pero bueno, vayamos  al tema de hoy. 

Tras consultar no pocos de los ejemplos que hay por Internet sobre cómo 
gestionar varios leds con tres pines de Arduino utilizando recursos
como el [Shift Register 74HC595]({{ site.baseurl }}{% link pages/shiftregister-74HC595.md %}), 
me surgen muchas dudas sobre intensidad de corriente y las resistencias.

Mi idea es dividir los leds del teclado en dos grupos de 32, de modo que cada uno
de estos bloques esté gestionado por cuatro Shift Registers 74HC595 montados en serie.
Pero claro, es muy distinto que en un bloque de 32 leds esté encendido solo uno de 
ellos a que estén encendidos todos. Al menos a priori da la sensación de que
debería controlarse la corriente para que la luminosidad de los leds se la misma
en ambos casos y que no se vean con menos brillo a medidad que hay más leds 
encendidos.

Y, aunque visualmente quizás no se perciba demasiado, entiendo que igualmente 
a nivel del circuito debería tenerse en cuenta esta circunstancia si queremos
ser correctos.

Veamos las magnitudes en los dos casos extremos.

Con un led de los 32 encencido:




Con los 32 leds encendidos:



Vamos a verificarlo con el multímetro a ver qué obtenemos.