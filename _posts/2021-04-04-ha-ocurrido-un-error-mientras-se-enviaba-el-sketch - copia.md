---
layout: post
title:  Error al subir el sketch
permalink: /blog/:day-:month-:year/pantallas.html
location: Mora de Rubielos
pygment_theme: default
main_image: /assets/img/blog/2021-04-04/error-subir-small.png
---
Hoy, al trabajar con el proyecto en un equipo distinto del habitual, me he encontrado con la siguiente sorpresa de que al subir el sketch se quedaba indefinidamente en estado "Subiendo", y si lo volvía a intentar, entonces ya me aparecía al m ensaje 

```
Ha habido un error mientras se enviaba el skeTch
```

{% assign img_url = "/assets/img/blog/2021-04-04/error-subiir-sketch.png" %}
{% assign img_description = "Error tal cual se muestra en el IDE" %}
{% include blog/one-image.html %}

Otro de los síntomas extraños con los que me he encontrado, es que en el IDE de Arduino aparecía disponible permanentemente el puerto COM1, tanto si tenía la placa conectada como si no.

Me he percatado de que el dispositivos aparecía esto:

{% assign img_url = "/assets/img/blog/2021-04-04/error-dispositivos.png" %}
{% assign img_description = "FT232R USB UART" %}
{% include blog/one-image.html %}


He descargado el driver https://www.usb-drivers.org/ft232r-usb-uart-driver.html

Luego he hecho clic derecho sobre el dispositivo indicado en rojo y he elegido "Actualizar controlador". Después "Examinar mi PC en busca de controladores" y he seleccionado "CDM v2.08.28 Certified" desde la carpeta donde la había descargado. La instalación se ha producido sin problema y tras el reinicio del equipo ya me aparecía un nuevo puerto COM3 que me ha fucionado perfectamente desde el IDE de Arduino.

{% assign img_url = "/assets/img/blog/2021-04-04/OK-dispositivos.png" %}
{% assign img_description = "USB Serial Port (COM3)" %}
{% include blog/one-image.html %}

He guardado el driver para su [descarga directa](/assets/drivers/CDM-2.08.28-WHQL-Certified1.zip) si alguien lo necesitara.
