---
layout: default
title: El Tablero
header_image: chessboard/chessboard-1.jpeg
header_text: El tablero
subheader_text: Preparativos básicos
header_height: 300px
creation_date: 21/07/2021
creation_location: Mora de Rubielos
last_update_date: 21/06/2023
last_update_location: Mora de Rubielos
---
## Objetivo
---
Vamos a transformar el tablero físicamente para que nos permita indicar nuestros 
movimientos (los del jugador humano) y Stockfish (el jugador de software) pueda hacer lo propio con 
los suyos. En esta primera versión de ChessPU, esto
lo haremos mediante leds que señalán qué piezas
hay que mover y adónde. En próximas versiones, la idea es que unos sensores
magnéticos interpreten directamente los movimientos naturales del jugador humano.
### Perforación y etiquetado
---
En cada uno de los escaques vamos a incrustar un led azul de 3 milímetros. Para ello, 
haremos una marca en cada una de las casillas exactamente en la
misma posición que indicará el lugar donde perforaremos para introducir el led. 
Importante que la marca la hagamos cerca de uno de los 
laterales o __en una esquina__, de modo que al posar la pieza esta no tape
completamente el led, o lo deje oculto al jugador por quedar la pieza delante.

{% assign img1_url = "/assets/img/chessboard/chessboard-marks-1.jpg" %}
{% assign img1_description = "Hay muchas formas de hacer esto. Yo he empleado una plantilla que viene con mi
juego de brocas. He recurrido al agujero de la parte inderior izquierda para hacer una marca con rotulador." %}
{% assign img1_style = "border: 1px solid silver; padding: 8px;" %}
{% assign img2_url = "/assets/img/chessboard/chessboard-marks-3.jpg" %}
{% assign img2_description = "Una vez tenemos marcadas todas las casillas, procederemos a perforar con una broca de 3 mm. Los leds encajarán perfectamente en estos agujeros." %}    
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

### Leds
---
Como comentamos arriba, vamos a incrustar en cada casilla un led azul de 3 milímetros, lo que hace un total de 64. Cada uno de ellos trabaja con un voltaje de entre 3.0 y 3.2 V, por lo que irá acompañado de una resistencia de 220 Ω dispuesta en serie con él.

(Pendiente explicar el  VOLTAJE DE SALIDA DE LOS PINES Y EL MINICÁLCULO de la resistencia)

{% assign img1_url = "/assets/img/components/resistemcia-220-ohmnios.webp" %}
{% assign img1_description = "64 resistencias de 220 Ω" %}
{% assign img1_style = "border: 1px solid silver; padding: 8px;" %}
{% assign img2_url = "/assets/img/components/leds-azules-3mm.jpg" %}
{% assign img2_description = "64 leds azules de 3 mm" %}    
{% assign img2_style = "border: 1px solid silver; padding: 8px;" %}    
{% include page/two-images.html %}

Dado que a cada binomio led-resistencia le tiene que llegar un cable de alimentación y otro de conexión a tierra, a poco que nos descuidemos, la parte posterior del tablero puede acabar hecha una maraña de cables inmanejable. Podemos ver hasta que extremo de descontrol puede llegar esta situación en [esta entrada del blog]({{ site.url }}/blog/05-12-2020/el-reinicio.html) que ilustra una de las formas que experimenté (y descarté) de cablear y conectar los [74HC595]({{ site.url }}/pages/shiftregister-74HC595.html) (tema que se verá con detalle más adelante).

Para evitar este caos de cables y llegar de forma organizada a la parte posterior de cada casilla, podemos utilizar una cinta como la de la imagen que sigue. Tiene la ventaja de que se puede fijar fácilmente al tablero para ir separando hilos independientes hacia cada casilla.

{% assign img_url = "/assets/img/components/cinta-plana-10-pines.jpg" %}
{% assign img_description = "Cinta plana IDC de cable de arco iris 10 pines " %}
{% assign img_style = "border: 1px solid silver; padding: 8px; max-width: 400px;" %}
{% include page/one-image.html %}


La idea es desplegar una cinta de cable por fila, tal y como se muestra aquí

{% assign img_url = "/assets/img/chessboard/tablero-cableado-1.jpg" %}
{% assign img_description = "Cinta plana IDC de cable pegada y con un hilos dirigido a cada casilla de su fila" %}
{% assign img_style = "border: 1px solid silver; padding: 8px;" %}
{% include page/one-image.html %}

para conseguir finalmente algo parecido a esto

{% assign img_url = "/assets/img/chessboard/tablero-cableado-2.jpg" %}
{% assign img_description = "Oranización del cableado en la parte posterior del tablero." %}
{% assign img_style = "border: 1px solid silver; padding: 8px;" %}
{% include page/one-image.html %}

De momento, olvídemos de las plaquitas rojas que se ven en la imagen. Esto lo abordaremos en su momento.

