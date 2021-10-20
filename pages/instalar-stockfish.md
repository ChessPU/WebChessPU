---
layout: default
title: Instalar Stockfish
header_image: stockfish/stockfish-header.png
header_text: Stockfish
header_height: 300px
last_update_date: Miércoles 20/10/2021
last_update_location: Benissa
# diferentes estilos de código en http://jwarby.github.io/jekyll-pygments-themes/languages/java.html
---
## Stockfish
Stockfish es un motor de ajedrez de código abierto. Será nuestro rival en las partidas con ChessPU, encargándose de dar respuesta nuestros movimientos y de gestionar el juego en general. En [Wikipedia](https://es.wikipedia.org/wiki/Stockfish) hay una pequeña descripción de Stockfish que permite conocer algunos detalles sobre él.

Inicialmente, mientras estemos en el proceso de montaje del tablero, lo más cómodo será tenerlo instalado en nuestro Windows. De este modo podremos gestionarlo todo desde nuestro PC cómodamente. Más adelante ya abordaremos la instalación en Raspberry, que nos permitirá prescindir del ordenador y que el tablero sea completamente autónomo.

## Instalación
En primer lugar descargaremos Stockfish desde el [área de descarga](https://stockfishchess.org/download/) de la [web oficial](https://stockfishchess.org/). En mi caso he optado por la versión más compatible, no la más rápida.

{% assign img_url = "/assets/img/stockfish/stockfish-download.png" %}
{% assign img_description = "" %}
{% assign img_style = "border: 1px solid silver;" %}
{% include page/one-image.html %}

No se trata de un instalador ejecutable, sino de un fichero .zip que tendremos que desempaquetar en una carpeta de nuestra elección. Yo lo he hecho en C:\Stockfish, quedando finalmente instalado en C:\Stockfish\stockfish_14_win_x64_popcnt.

{% assign img_url = "/assets/img/stockfish/stockfish-directory.png" %}
{% assign img_description = "" %}
{% assign img_style = "border: 1px solid silver;" %}
{% include page/one-image.html %}

## Nociones
Para interactuar con Stockfish utilizaremos [UCI (Universal Chess Interface)](https://backscattering.de/chess/uci/).