---
layout: default
title: Gestionando los leds
header_image: chips/composition-74HC595-1.jpeg
header_text: Gestionando los leds
header_height: 300px
# diferentes estilos de código en http://jwarby.github.io/jekyll-pygments-themes/languages/java.html
---

Para controlar los 64 leds del tablero empleando pocos pines de nuestra placa Arduino, 
vamos a utilizar 8 chips [Shift Register 74HC595]({{ site.url }}/pages/shiftregister-74HC595.html)
conectados en serie. Dos módulos de expansión IO SPI para Raspberry Pi, que integran cuadtro 74HC595 cada uno, 
cumplirán perfectamente con esta misión. Cada módulo controlará 32 leds.

{% assign img_url = "/assets/img/components/expansion-32-gpio-7.jpg" %}
{% assign img_description = "Módulo de Expansión IO SPI de Raspberry Pi" %}
{% assign img_style = "border: 1px solid silver; padding: 16px;" %}
{% include page/one-image.html %}

Aunque estas placas se pueden conectar en cascada, para simplificar la instalación física en el 
teclado y la detección de posibles problemas, las instalaremos por separado. Una gestinará la
mitad superior del tablero (placa 2 de las im´sgenes de abajo) y la otra la mitad inferior (placa 1 de las imágenes de abajo).

{% assign img1_url = "/assets/img/misc/placas-en-tablero-1.png" %}
{% assign img1_description = "Ubicación de las placas en el tablero boca abajo" %}
{% assign img1_style = "border: 1px solid silver; padding: 16px;" %}
{% assign img2_url = "/assets/img/misc/plaquitas2.png" %}
{% assign img2_description = "Detalle de las placas en el tablero" %}
{% assign img2_style = "border: 1px solid silver; padding: 16px;" %}
{% include page/two-images.html %}


Teniendo en cuenta el esquema de pines del GPIO (General Purpose Input/Output) de Raspberry, en la plaquita 1 emplearemos
los pines numerados del 1 al 5 de la imagen de abajo para conectarla con Arduino:

{% assign img1_url = "/assets/img/raspberry/raspberry-pines-gpio.png" %}
{% assign img1_description = "Pines del GPIO de Raspberry" %}
{% assign img1_style = "border: 1px solid silver; padding: 16px;" %}
{% assign img2_url = "/assets/img/misc/expansion-gpio-arduino-3.png" %}
{% assign img2_description = "Conexiones desde Arduino a la plaquita 1" %}
{% assign img2_style = "border: 1px solid silver; max-height: 355px; padding: 16px;" %}
{% include page/two-images.html %}

### Configuración básica

Las conexiones que hay que hacer para que funcione el código básico de pruebas publicado el domingo 28/02/2021 en [GitHub](https://github.com/ChessPU/CheesPU/commit/2c5419ae76947343398257d88c867b60a352dc65) son las que se describen a continuación:

En la placa Arduino, tal y como se muestra en la foto que sigue, usaremos los pines digitales del 2 al 6 para gestionar los leds del tablero.

2 (verde), 3 (blanco) y 4 (amarillo) controlarán 32 leds de la parte inferior del tablero (filas de la 1 a la 4)


5 (verde), 6 (blanco) y 7 (amarillo) controlarán 32 leds de la parte superior del tablero (filas de la 5 a la 8)

{% assign img_url = "/assets/img/misc/conexiones-v1/chesspu-conexiones-1.webp" %}
{% assign img_description = "Conexión básica de tablero a Arduino" %}
{% assign img_style = "border: 1px solid silver; padding: 16px;" %}
{% include page/one-image.html %}

El primer grupo de tres (pines del 2 al 4) se conectará al primer módulo de expansión (el que queda más cerca a nuestra derecha) siguiendo el esquema de colores que es indica abajo, donde la alimentación (entrada 1 - roja) se conectará a la salida de 3.3 V de Arduino y la toma de tierra (entrada 2 negra) irá con una resistencia intemediando conectada a la toma de tierra de Arduinio.

{% assign img_url = "/assets/img/misc/expansion-gpio-arduino-3.png" %}
{% assign img_description = "Conexiones desde Arduino a la plaquita 1" %}
{% assign img_style = "border: 1px solid silver; max-height: 355px; padding: 16px;" %}
{% include page/one-image.html %}

El segundo grupo de tres (pines del 5 al 7) se conectará al segundo módulo de expansión (el que queda arriba a la derecha), siguiendo el mismo esquema de colores, pero sin hacer conexiones de alimentación ni tierra.

Además, por la parte de abajo de la primera plaquita conectaremos la tierra del circuito de leds del tablero al pin  que se indica a continuación

{% assign img_url = "/assets/img/misc/conexiones-v1/chesspu-conexiones-2.jpeg" %}
{% assign img_description = "Toma de tierra del tablero" %}
{% assign img_style = "border: 1px solid silver; max-height: 450px; padding: 16px;" %}
{% include page/one-image.html %}
