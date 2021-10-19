---
layout: default
title: Instalar Stockfish
header_image: stockfish/stockfish-14.png
header_text: Stockfish
header_height: 300px
# diferentes estilos de código en http://jwarby.github.io/jekyll-pygments-themes/languages/java.html
---
Stockfish es un motor de ajedrez de código abierto que utilizaremos como rival en nuestras partidas con ChessPU. Se puede consultar la [Wikipedia](https://es.wikipedia.org/wiki/) para tener una descripción un poco más amplia y conocer algunos detalles.

Inicialmente, mientras estemos construyendo nuestro tablero, lo más cómodo será instalarlo en nuestro Windows para gestionarlo todo desde nuestro PC. Más adelante ya haremos la instalación en Raspberry para poder así prescindir del ordenador y que el tablero sea completamente autónomo.

En primer lugar descargaremos Stockfish desde su [web oficial](https://stockfishchess.org/). Yo de momento he optado por la versión más compatible, no la más rápida.

{% assign img_url = "/assets/img/stockfish/stockfish-download.png" %}
{% assign img_description = "Descr" %}
{% assign img_style = "max-height: 1000px; border: 1px solid gray;" %}
{% include page/one-image.html %}

No se trata de un instalador ejecutable, sino de un fichero .zip que tendremos que desempaquetar en una carpeta de nuestra elección. Yo lo he hecho en la que se puede ver en la imagen que sigue:

{% assign img_url = "/assets/img/stockfish/stockfish-directory.png" %}
{% assign img_description = "Descr" %}
{% assign img_style = "max-height: 1000px;  border: 1px solid gray;" %}
{% include page/one-image.html %}
