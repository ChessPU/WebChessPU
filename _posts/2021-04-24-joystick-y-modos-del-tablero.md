---
layout: post
title: Joystick y modos del tablero
location: Mora de Rubielos
pygment_theme: native
main_image: /assets/img/blog/2021-04-24/joystick-code.png
---
Mejoras en el módulo de gestión del joystick implementando, entre otras cosas,
la captura de la pulsación.

He invertido mucho más tiempo del previsto porque parece que cualquier pin
digital no era válido. Me ha funcionado con el 2 y el 13, optando por este
último que estaba todavía libre.

{% assign img_url = "/assets/img/blog/2021-04-24/joystick-code.png" %}
{% assign img_description = "Fragmento de código del módulo joystick.ino" %}
{% include blog/one-image-wide.html %}