---
layout: post
title: Raspberry. Conectando.
location: Mora de Rubielos
pygment_theme: native
main_image: /assets/img/raspberry/raspberry-update.jpg
---
Tan sencillo como conectar por cable la salida Ethernet de la placa con el router y *voilà*, ya tenía conexión a Internet.

##### Actualizar
Lo primero que he hecho es actualizar el sistema ejecutando desde la línea de comandos lo siguiente:

```console

    sudo apt update
    sudo apt full-upgrade

```
https://www.raspberrypi.com/documentation/computers/os.html
Me he inspirado en las indicaciones de

Como mi conexión no es precisamente ultra rápida, ha tardado un ratito, pero el proceso ha concluido sin contratiempos.

##### Pequeños ajustes
Una de las cosas que más me está molestando es que, en cuanto me descuido, la placa se pone en modo de ahorro de energía y la pantalla se apaga. Las indicaciones para desactivar el modo de ahorro de energía están en [esta página](https://forums.raspberrypi.com/viewtopic.php?t=43932). 


##### Python
La versión de Python que aparece es un poco antigua; la voy a actualizar.
