---
layout: default
title: El Tablero
header_image: chessboard/chessboard-1.jpeg
header_text: El tablero
subheader_text: Preparativos básicos
header_height: 300px
last_update_date: Miércoles 21/07/2021
last_update_location: Mora de Rubielos
---
Vamos a transformar el tablero físicamente para que nos permita indicar nuestros 
movimientos (los del jugador humano) y Stockfish (el jugador de software) pueda hacer lo propio con 
los suyos. En esta primera versión de ChessPU, esto
lo haremos mediante leds que señalán qué piezas
hay que mover y adónde. En próximas versiones, la idea es que unos sensores
magnéticos interpreten directamente los movimientos naturales del jugador humano.
#### Perforación, etiquetado y leds

En cada uno de los escaques vamos a incrustar un led de 3 milímetros. Para ello, 
haremos una marca en cada una de las casillas exactamente en la
misma posición que indicará el lugar donde perforaremos para introducir el led. 
Importante que la marca la hagamos cerca de uno de los 
laterales o __en una esquina__, de modo que al posar la pieza esta no tape
completamente el led, o lo deje oculto al jugador por quedar la pieza delante.

        {% assign img1_url = "/assets/img/chessboard/chessboard-marks-1.jpg" %}
        {% assign img1_description = "Hay muchas formas de hacer esto. Yo he empleado una plantilla que viene con mi
juego de brocas. He recurrido al agujero de la parte inderior izquierda para 
hacer una marca con rotulador." %}
        {% assign img1_style = "border: 1px solid silver; padding: 8px;" %}
        {% assign img2_url = "/assets/img/chessboard/chessboard-marks-3.jpg" %}
        {% assign img2_description = "Una vez tenemos marcadas todas las casillas, procederemos a perforar con una 
broca de 3 mm. Los leds encajarán perfectamente en estos agujeros." %}    
        {% assign img2_style = "border: 1px solid silver; padding: 8px;" %}    
        {% include page/two-images.html %}

Ahora, antes de seguir adelante, vamos a etiquetar cada uno de los escaques por
su parte posterior. Lo haremos empleando la clásica __notación algebraica__.

{% assign img1_url = "/assets/img/chessboard/algebraic-notation.jpg" %}
{% assign img1_style = "border: 1px solid silver; padding: 0px;" %}
{% assign img1_description = "" %}
{% assign img2_url = "/assets/img/chessboard/chessboard-labels-1.jpg" %}
{% assign img2_style = "border: 1px solid silver; padding: 8px;" %}
{% assign img2_description = "Obteniendo algo como esto" %}
{% include page/two-images.html %}



