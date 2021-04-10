---
layout: post
title:  Problema subiendo a la placa
permalink: /blog/:day-:month-:year/pantallas.html
location: Mora de Rubielos
pygment_theme: default
---
Hoy una nueva sorpresa. Al subir el sketch a la placa me ha aparecido el error "Problema subiendo a la placa. Visita http://www.arduino.cc/en/Guide/Troubleshooting#upload para sugerencias.", acompañado de mensajes como los siguientes:

```
...
avrdude: stk500_recv(): programmer is not responding
avrdude: stk500_getsync() attempt 1 of 10: not in sync: resp=0xdd
avrdude: stk500_recv(): programmer is not responding
avrdude: stk500_getsync() attempt 2 of 10: not in sync: resp=0xdd
...
```

{% assign img_url = "/assets/img/blog/2021-04-10/error-arduino.png" %}
{% assign img_description = "Error tal cual se muestra en el IDE" %}
{% include blog/one-image.html %}

Otro de los síntomas extraños con los que me he encontrado, es que en el IDE de Arduino aparecía disponible permanentemente el puerto COM1, tanto si tenía la placa conectada como si no.

Me he percatado de que en dispositivos aparecía esto:

{% assign img_url = "/assets/img/blog/2021-04-10/error-dispositivos.png" %}
{% assign img_description = "USB2-0-Seriel" %}
{% include blog/one-image.html %}


Para solucionarlo, he descargado el driver CH341SER.ZIP desde http://www.wch.cn/download/CH341SER_ZIP.html y he ejecutado el instalador que tiene el aspecto siguiente:

{% assign img_url = "/assets/img/blog/2021-04-10/instalar-driver.png" %}
{% assign img_description = "USB-Serial CH340" %}
{% include blog/one-image.html %}

Tras la instalación y de forma inmediata ya me ha aparecido lo siguiente:



{% assign img_url = "/assets/img/blog/2021-04-10/dispositivos-ok.png" %}
{% assign img_description = "USB-SERIAL CH340 Port (COM4)" %}
{% include blog/one-image.html %}

Y en el IDE de Arduino me ha aparecido el puerto como disponible:

{% assign img_url = "/assets/img/blog/2021-04-10/ok-com-ide.png" %}
{% assign img_description = "USB-SERIAL CH340 Port (COM4)" %}
{% include blog/one-image.html %}

He guardado el driver para su [descarga directa](/assets/drivers/CH341SER.ZIP) por si alguien lo necesitara.

