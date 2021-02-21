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
los pines numerados del 1 al 5 de la imagen de bajoa para conectarla con Arduino:

{% assign img1_url = "/assets/img/raspberry/raspberry-pines-gpio.png" %}
{% assign img1_description = "Pines del GPIO de Raspberry" %}
{% assign img1_style = "border: 1px solid silver; padding: 16px;" %}
{% assign img2_url = "/assets/img/misc/expansion-gpio-arduino-3.png" %}
{% assign img2_description = "Conexiones desde Arduino a la plaquita 1" %}
{% assign img2_style = "border: 1px solid silver; max-height: 355px; padding: 16px;" %}
{% include page/two-images.html %}


