---
layout: post
title:  Arduino - Problema subiendo a la placa
# permalink: /blog/:day-:month-:year/pantallas.html
location: Mora de Rubielos
pygment_theme: native
---
Hoy una nueva sorpresa: al subir el sketch a la placa me ha aparecido el error *"Problema subiendo a la placa. Visita http://www.arduino.cc/en/Guide/Troubleshooting#upload para sugerencias."*, acompañado de mensajes como los siguientes:

```c++
    
    ...
    avrdude: stk500_recv(): programmer is not responding
    avrdude: stk500_getsync() attempt 1 of 10: not in sync: resp=0xdd
    ...

```
En concreto el error tenía el siguiente aspecto en el IDE de Arduino:

{% assign img_url = "/assets/img/blog/2021-04-10/error-arduino.png" %}
{% assign img_description = "Error tal cual se muestra en el IDE" %}
{% include blog/one-image-wide.html %}

Otro de los síntomas extraños con los que me he encontrado, es que en el IDE de Arduino aparecía disponible permanentemente el puerto COM1, tanto si tenía la placa conectada como si no. He accedido al administrador de dispositivos de Windows y aparecía un problema con dispositivo USB como se puede apreciar en el recuadro azul:

{% assign img_url = "/assets/img/blog/2021-04-10/error-dispositivos.png" %}
{% assign img_description = "USB2-0-Seriel" %}
{% include blog/one-image.html %}

Para solucionarlo, he descargado el driver CH341SER.ZIP [desde](http://www.wch.cn/download/CH341SER_ZIP.html) (descarga local más abajo), y he ejecutado el instalador que tiene el aspecto siguiente:

{% assign img_url = "/assets/img/blog/2021-04-10/instalar-driver.png" %}
{% assign img_description = "USB-Serial CH340" %}
{% include blog/one-image.html %} 

Tras la instalación, se ha corregido de forma inmediata el problema de USB en el administrador de dispositivos, y también ha aparecido  disponible el nuevo puerto COM en el IDE de Arduino:

        {% assign img1_url = "/assets/img/blog/2021-04-10/dispositivos-ok.png" %}
        {% assign img1_description = "Puerto USB-SERIAL CH340 Port (COM4) operativo" %}
        {% assign img1_style = "padding: 12px; border: 1px solid silver;" %}
        {% assign img2_url = "/assets/img/blog/2021-04-10/ok-com-ide.png" %}
        {% assign img2_description = "Puerto operativo en el IDE de Arduino" %}    
        {% assign img2_style = "border: 2px solid silver;" %}    
        {% include blog/two-images.html %}

---

#### Enlaces de interés
 - Descarga directa (local) del [driver USB-Serial CH340](/assets/drivers/CH341SER.ZIP).

