---
layout: default
title: El Tablero
header_image: chessboard/chessboard-1.jpeg
header_text: El tablero
header_height: 300px
---
Vamos a transformar el tablero de forma que nos permita indicar nuestros 
movimientos de jugador humano a Stockfish, y Stockfish nos pueda indicar 
los suyos. En esta primera versión del tablero, tod esto
lo haremos mediante leds que nos señalán de diferentes modos qué piezas
hay que mover y adónde. En próximas versiones, la idea es que unos sensores
magnéticos tomen direcamente los movimientos del jugador humano.
#### Perforación, etiquetado y leds

En cada uno de los escaques vamos a incrustar un led de 3 milímetros.

Para ello, haremos una marca en cada una de las casillas exacatamente en la
misma posición. Importante que la marca la hagamos cerca de uno de los 
laterales o __en una esquina__, de modo que al posar la pieza, esta no tape
completamente el led o lo deje oculto al jugador por quedar la pieza delante.

Hay muchas formas de hacer esto. Yo he empleado una plantilla que viene con mi
juego de brocas. He recurrido al agujero de la parte inderior izquierda para 
hacer una marca con rotulador.

{% assign img_url = "/assets/img/chessboard/chessboard-marks-1.jpg" %}
{% assign img_description = "" %}
{% include blog/one-image.html %}

Una vez tenemos marcadas todas las casillas, procederemos a perforar con una 
broca de 3 mm. Los leds encajarán perfectamente en estos agujeros.

{% assign img_url = "/assets/img/chessboard/chessboard-marks-3.jpg" %}
{% assign img_description = "" %}
{% include blog/one-image.html %}

Ahora, antes de seguir adelante, vamos a etiquetar cada uno de los escaques por
su parte posterior. Lo haremos empleando la clásica __notación algebraica__.

{% assign img_url = "/assets/img/chessboard/algebraic-notation.jpg" %}
{% assign img_description = "" %}
{% include blog/one-image.html %}

Obteniendo algo como esto:

{% assign img_url = "/assets/img/chessboard/chessboard-labels-1.jpg" %}
{% assign img_description = "" %}
{% include blog/one-image.html %}


