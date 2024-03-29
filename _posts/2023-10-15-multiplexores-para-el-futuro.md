---
layout: post
title: Multiplexores para el futuro
location: Mora de Rubielos
pygment_theme: native
main_image: /assets/img/blog/2023-10-15/CD74HC4067.jpg
---
En versiones futuras de ChessPU quiero utilizar la detección automática de las
piezas mediante imanes, por lo que necesitaré simplificar la gestión de la 
entrada de información desde cada una de las 64 casillas del tablero. Para ello, acabo de
comprar en Amazon varias unidades de [CD74HC4067 CMOS 16 Canales 16 CH Digital
Multiplexor](https://amzn.eu/d/dlAJI7a).

Para aprender a manejarlos, recojo aquí algunos artículos interesantes que he
encontrado y que me pueden servir como punto de partida

* [Artículo muy claro y cuidado en luisllamas.es](https://www.luisllamas.es/mas-salidas-y-entradas-en-arduino-con-multiplexor-cd74hc4067/).

* [Artículo interesante en Prometec](https://www.prometec.net/multiplexor-74hc4067/)

* [Uso es cascada](https://forum.arduino.cc/t/multiple-multplexer-cdhc4067/632747)

Hay muchos productos muy parecidos, como por ejemplo [este](https://amzn.eu/d/88SyM11), 
pero vamos a ver si con los que he comprado hay suerte. De momento no tengo 
experiencia ni criterio como para distinguir los matices de unos y otros.

La idea es utilizar estos multiplexores para leer el estado de unos
**interruptores magnéticos** situados debajo de cada casilla y que reaccionarán
a la existencia o no de una pieza de ajedrez ubicada encima que lleva
incorporado un imán. En su momento compré [este modelo](https://amzn.eu/d/7UPyihs) 
con el que hice algún experimento con resultado positivo, pero se pueden
comprar en mayor cantidad y a mejor precio ([ejemplo](https://amzn.eu/d/8bJKoLh)).

        {% assign img_url = "/assets/img/blog/2023-10-15/interruptor_magnetico.jpg" %}
        {% assign img_description = "Gebildet 10pcs 4W 3 Pin Vidrio Reed Interruptor" %}
        {% assign img_style = "" %}
        {% include blog/one-image.html %}