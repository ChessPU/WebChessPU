---
layout: default
title: Instalar Stockfish
header_image: stockfish/stockfish-header.png
header_text: Stockfish
header_height: 300px
last_update_date: Miércoles 21/10/2021
last_update_location: Benissa
# pygment_theme: native
# diferentes estilos de código en http://jwarby.github.io/jekyll-pygments-themes/languages/java.html
---
## Stockfish
---
Stockfish es un motor de ajedrez de código abierto. Será nuestro rival en las partidas con ChessPU, encargándose de dar respuesta nuestros movimientos y de gestionar el juego en general. En [Wikipedia](https://es.wikipedia.org/wiki/Stockfish) hay una pequeña descripción de Stockfish que permite conocer algunos detalles sobre él. Si queremos profundizar, podemos acceder al [proyecto oficial en GitHub](https://github.com/official-stockfish/Stockfish).

Inicialmente, mientras estemos en el proceso de montaje del tablero, lo más cómodo será tenerlo instalado en nuestro Windows. De este modo podremos gestionarlo todo desde nuestro PC cómodamente. Más adelante ya abordaremos la instalación en Raspberry, que nos permitirá prescindir del ordenador y que el tablero sea completamente autónomo.

## Instalación
---
En primer lugar descargaremos Stockfish desde el [área de descarga](https://stockfishchess.org/download/) de la [web oficial](https://stockfishchess.org/). En mi caso he optado por la versión más compatible, no la más rápida.

{% assign img_url = "/assets/img/stockfish/stockfish-download.png" %}
{% assign img_description = "Página de descarga de Stockfish" %}
{% assign img_style = "border: 1px solid silver;" %}
{% include page/one-image.html %}

No se trata de un instalador ejecutable, sino de un fichero .zip que tendremos que desempaquetar en una carpeta de nuestra elección. Yo lo he hecho en C:\Stockfish, quedando finalmente instalado en C:\Stockfish\stockfish_14_win_x64_popcnt.

{% assign img_url = "/assets/img/stockfish/stockfish-directory.png" %}
{% assign img_description = "Stocksfish instalado (sencillamente desempaquetado)" %}
{% assign img_style = "border: 1px solid silver;" %}
{% include page/one-image.html %}

## Nociones
---
Stockfish utiliza [UCI (Universal Chess Interface)](https://backscattering.de/chess/uci/). Dispone de la mayoría de las opciones UCI descritas en [este documento](https://www.shredderchess.com/download/div/uci.zip) que podemos descargar.

Para utilizarlo e interactuar con él de forma directa hay que lanzar el ejecutable (en mi caso stockfish_14_x64_popcnt.exe), lo que abrirá una ventana de consola típica en la que, dejando a un lado las opciones de configuración y otras cuestiones, lo más directo y elemental que cabe destacar es que, **cada vez que queramos obtener un movimiento de Stockfish, tenemos que proporcionarle la disposición completa del tablero**. De hecho, en la descripción oficial del UCI se dice de forma explícita que "Before the engine is asked to search on a position, there will always be a position command to tell the engine about the current position".

La forma más sencilla de comunicarle el estado del tablero es utilizando la [notación FEN](https://ajedrez.pro/notacion-fen) (Forsythe-Edwards Notation).

{% assign img_url = "/assets/img/stockfish/stockfish-console.png" %}
{% assign img_description = "Stockfish en ejecución en Windows" %}
{% assign img_style = "border: 1px solid silver;" %}
{% include page/one-image.html %}

En la imagen de arriba se puede ver cómo en la primera línea señalada se le indica a Stockfish la situación actual de juego 

```
    position fen rnbqkbnr/pp1ppppp/8/2p5/4P3/5N2/PPPP1PPP/RNBQKB1R b KQkq - 1 2
```

En la segunda línea destacada se le pide un movimiento a Stockfish (limitado a 250 segundos de análisis). 

```
    go movetime 250
```

Y el resultado nos aparece en la línea señalada con la flecha roja al final, indicando con "bestmove" el que Stockfish considera el mejor movimiento y mostrando con "ponder" la que probablemente sea la respuesta del contrincante.

```
    bestmove d7d6 ponder d2d4
```

