---
layout: post
title: Raspberry. Sin sonido...
location: Mora de Rubielos
pygment_theme: native
main_image: /assets/img/raspberry/speakers-2.jpg
---
En principio no tengo intención de sacar partido a las prestaciones de audio de la Raspberry en este proyecto, pero para asegurarme de que puedo hacerlo si lo necesitara, he conectado unos pequeños altavoces alimentados por USB. El resultado ha sido un **fracaso total**. 

Resulta que lo que yo pensaba que era una clásica salida de audio, en realidad es una salida de audio estéreo compartida con la salida de vídeo compuesto (RCA).

{% assign img_url = "/assets/img/raspberry/video-rca.jpg" %}
{% assign img_description = "" %}
{% assign img_style = "" %}
{% include blog/one-image.html %}

##### Más adminículos
Voy a tratar de compensar mi ignorancia en estas cuestiones con accesorios. Acabo de comprar en Amazon estos dos a ver si así consigo conectar unos altavoces convencionales a la Raspberry.

{% assign img1_url = "/assets/img/raspberry/audio-wire-2.jpg" %}
{% assign img1_description = "Cable 3RCA Macho - Jack 4C Macho 3,5mm" %}
{% assign img1_style = "max-height: 350px;" %}
{% assign img2_url = "/assets/img/raspberry/audio-wire-1.jpg" %}
{% assign img2_description = "Conector 3,5mm Jack Hembra a 2 Conectores RCA Hembra," %}     
{% assign img2_style = "" %}    
{% include blog/two-images.html %}

Cuando los tenga, escribiré otra entrada con el resultado. No sé... Me parece un poco rebuscado tanto adaptador para obtener una sencilla salida de audio, pero como mi incompetencia sobre esta cuestión es total, pues probaré.