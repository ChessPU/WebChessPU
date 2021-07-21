---
layout: default
title: El Tablero
header_image: chessboard/chessboard-1.jpeg
header_text: El tablero
header_height: 300px
---
Vamos a transformar el tablero de forma que nos permita proporcionar 
indicaciones al jugador y también recoger sus movimientos. Lo primro lo haremos
mediante lefs, y lo segundo mediante sensores magnéticos. Unos y otros los
gestionaremos con Arduino y algunos circuitos integrados adicionales.

Vamos a transformar el tablero de forma que nos permita proporcionar 
indicaciones al jugador y también recoger sus movimientos. Lo primero lo haremos
mediante lefs, y lo segundo mediante sensores magnéticos. Unos y otros los
gestionaremos con Arduino y algunos circuitos integrados adicionales.

#### Perforación, etiquetado y leds

En cada uno de los escaques vamos a incrustar un led de 3 milímetros.

Para ello, haremos una marca en cada una de las casillas exacatamente en la
misma posición. Importante que la marca la hagamos cerca de uno de los 
laterales o __en una esquina__, de modo que la al posar la pieza, ésta no tape
completamente el led o lo deje oculto al jugador por quedar la pieza delante.

Hay muchas formas de hacer esto. Yo he empleado una plantilla que viene con mi
juego de brocas. He recurrido al agujero de la parte inderior izquierad para 
hacer una marca con rotulador.

![image]({{ site.baseurl }}{{ site.imagespath }}chessboard/chessboard-marks-1.jpg){: .img-fluid}

Una vez tenemos marcadas todas las casillas, procederemos a perforar con una 
broca de 3 mm. Los leds encajarán perfectamente en estos agujeros.

![image]({{ site.baseurl }}{{ site.imagespath }}chessboard/chessboard-marks-3.jpg){: .img-fluid}

Ahora, antes de seguir adelante, vamos a etiquetar cada uno de los escaques por
su parte posterior. Lo haremos empleando la clásica __notación algebraica__.

![image]({{ site.baseurl }}{{ site.imagespath }}chessboard/algebraic-notation.jpg){: .img-fluid}

Obteniendo algo como esto:

![image]({{ site.baseurl }}{{ site.imagespath }}chessboard/chessboard-labels-1.jpg){: .img-fluid}

