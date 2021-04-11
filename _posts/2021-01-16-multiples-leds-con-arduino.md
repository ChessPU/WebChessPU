---
layout: post
title: Múltiples leds con Arduino
permalink: /blog/:day-:month-:year/multiples-leds-con-arduino
location: Mora de Rubielos
main_image: /assets/img/personal/virgen-de-la-vega-1-16-01-2021-2.jpeg
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

Mi idea es dividir los leds del tablero en dos grupos de 32, de modo que cada uno
de estos bloques esté gestionado por cuatro Shift Registers montados en cascada.
Pero claro, es muy distinto que en un bloque de 32 leds esté encendido solo uno de 
ellos a que estén encendidos todos. Al menos a priori, da la sensación de que
debería controlarse la corriente para que la luminosidad de los leds sea la misma
en todos los casos casos y que no se vean con menos brillo a medida que hay más leds 
encendidos.

Cabe la posibilidad de que la diferencia de brillo sea despreciable y apenas se perciba,
pero voy a analizarlo un poco para tratar de hacer un planteamiento lo más correcto posible.

Para simplificar el montaje, vamos a utilizar una placa que ya aporta los cuatro
Shift Register en cascada. Se trata de la Referencia Rxp1y3ref56 de la marca Richer 
que, aunque está pensada para Raspberry, podemos usarla también con Arduino 
alimentándola con la salida de 3.3 V de nuestro Arduino.

{% assign img_url = "/assets/img/components/expansion-32-gpio-1.jpg" %}
{% assign img_style = "max-height: 300px;" %}
{% assign img_description = "Richer-R Tarjeta de Módulo de Expansión 32 GPIO" %}
{% include blog/one-image.html %}

Los pines de control no son lógicamente los que proporcionan la alimentación a los leds, sino que se
ocupan de establecer cuáles se han de encender. Esto
quiere decir que en todos los casos, con independencia de la cantidad de leds
encendidos, cada uno de ellos está sometido a una tensión de 3.3 V (constatado además 
con el multímetro), por lo que lo único que tendremos que controlar es la intensidad
de corriente.



---------
PENDIENTE
---------
Dirimir si en los pines de control, que salen de Arduino con 5 V tenemos que poner un 
divisor de tensión para que a la plaquita le lleguen solo 3.3 V.

En las especificaciones de la plaquita:

Voltaje de funcionamiento: 2.4v-5v

Voltaje de IO: 3.3v

Amplió 32 IO unidireccional
Conexión a través de SPI
Frecuencia de cambio de 100 MHz (típica)
Entrada en serie de 8 bits
Salida serial o paralela de 8 bits
Especificado de -40C a + 85C y de -40C a + 125C
Aplicación típica: maneje la pantalla del enrejado, pantalla numérica del conductor, LED de matriz de impulsión

Así que, por prudencia, los pines de control los llevaremos a un máximo de 3.3 V para evitar estar al límite de los 5 V
Lo he probado con utilizando los pines de salida de Arduino a 5 V, pero supone que es mejor estar dentro de la zona intermedia
del rango de voltaje.

Ahora, vamos a comprobar la intensidad de corriente...


Luego, teniendo en cuenta que el máximo de intensidad 
que puede proporcionar es de 20 mA 



Veamos las magnitudes en los dos casos extremos.

Con un led de los 32 encencido:




Con los 32 leds encendidos:



Vamos a verificarlo con el multímetro a ver qué obtenemos.