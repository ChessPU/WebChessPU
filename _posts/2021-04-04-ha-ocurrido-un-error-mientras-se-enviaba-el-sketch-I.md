---
layout: post
title:  Error al subir el sketch
permalink: /blog/:day-:month-:year/pantallas.html
location: Mora de Rubielos
pygment_theme: native
main_image: /assets/img/blog/2021-04-04/error-subir-small.png
---
Hoy, al trabajar con el proyecto en un equipo distinto del habitual, me he encontrado con la sorpresa de que al subir el sketch se quedaba indefinidamente en estado "Subiendo", y si lo volvía a intentar, entonces ya me aparecía al mensaje: 

```c++
    
    ...
    Ha habido un error mientras se enviaba el skeTch
    ...

```

{% assign img_url = "/assets/img/blog/2021-04-04/error-subiir-sketch.png" %}
{% assign img_description = "Error tal cual se muestra en el IDE" %}
{% include blog/one-image.html %}

Otro de los síntomas extraños con los que me he encontrado, es que en el IDE de Arduino aparecía disponible permanentemente el puerto COM1, tanto si tenía la placa conectada como si no. También me he percadato de que en dispositivos de Windows aparecía esto:

{% assign img_url = "/assets/img/blog/2021-04-04/error-dispositivos.png" %}
{% assign img_description = "FT232R USB UART" %}
{% include blog/one-image.html %}

Para solucionarlo, primero he descargado el driver [https://www.usb-drivers.org/ft232r-usb-uart-driver.html](https://www.usb-drivers.org/ft232r-usb-uart-driver.html) y luego he hecho clic derecho sobre el dispositivo indicado arriba en rojo y he elegido "Actualizar controlador". Después e ido "Examinar mi PC en busca de controladores" y he seleccionado "CDM v2.08.28 Certified" desde la carpeta donde lo había descargado. La instalación se ha producido sin problema y tras el reinicio del equipo ya me aparecía un nuevo puerto COM3 que me ha fucionado perfectamente desde el IDE de Arduino.

{% assign img_url = "/assets/img/blog/2021-04-04/OK-dispositivos.png" %}
{% assign img_description = "USB Serial Port (COM3)" %}
{% include blog/one-image.html %}

---

#### Enlaces de interés
- Descarga directa (local) del [driver](/assets/drivers/CDM-2.08.28-WHQL-Certified1.zip).
