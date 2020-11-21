---
layout: default
title: 
---
# El tablero
![image]({{ site.baseurl }}{{ site.imagespath }}chessboard/chessboard-1.jpeg){: .img-fluid}

Vamos a transformar el tablero de forma que nos permita proporcionar 
indicaciones al jugador y también recoger sus movimientos. Lo primro lo haremos
mediante lefs, y lo segundo mediante sensores magnéticos. Unos y otros los
gestionaremos con Arduino y algunos circuitos integrados adicionales.
## Perforación, etiquetado y leds
En cada uno de los escaques vamos a incrustar un led de 3 milímetros.

Para ello, haremos una marca en cada una de las casillas exacatamente en la
misma posición. Importante que la marca la hagamos cerca de uno de los 
laterales o en una esquina, de modo que la al posar la pieza, ésta no tape
completamente el led o quede oculto al jugador por quedar la pieza delante.

Hay muchas formas de hacer esto. Yo he empleado una plantilla que viene con mi
juego de brocas. He recurrido al agujero de la parte inderior izquiera para 
hacer una marca con rotulador.