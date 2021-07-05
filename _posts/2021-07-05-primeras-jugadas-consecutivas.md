---
layout: post
title: Primera secuencia de jugadas
location: Mora de Rubielos
pygment_theme: native
main_image: /assets/img/blog/2021-07-05/movements.png
---
¡Por fin se ha producido el **primer intercambio de jugadas entre humano
y Stockfish**!

A pesar de mi constancia en la inconstancia, hoy he hecho un pequeño gran
avance: la correcta interacción entre Stockfish, Python y Arduino me ha
permitido efectuar varios movimientos desde el tablero y obtener las 
correspondientes jugadas de respuesta del motor de juego.

La señalización de las jugadas humanas y de Stockfish a través de los leds
todavía está pendiente de concluir, pero con lo implementado hasta ahora
y la representación en pantalla del tablero, ya he podido jugar.

{% assign img_url = "/assets/img/blog/2021-07-05/movements.png" %}
{% assign img_description = "Visualización de la secuencia de jugadas en la salida de Python" %}
{% include blog/one-image-wide.html %}

La verdad es que este paso me anima a continuar. Las piezas que hasta ahora
estaba preparando de forma independiente han empezado a encajar y el resultado
es muy prometedor.

El paso siguiente que tengo previsto es concluir la señalización mediante leds
de los movimientos del jugador humano, e implementar la señalización de los 
movimiendos de Stockfish.