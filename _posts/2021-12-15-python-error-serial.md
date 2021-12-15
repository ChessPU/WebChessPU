---
layout: post
title: Error con Python
location: Mora de Rubielos
pygment_theme: native
main_image: /assets/img/blog/2021-12-15/error-python.png
---
De forma absolutamente inopinada, me he encontrado de buenas a primeras con el error que se puede ver en la imagen de cabecera.

Después de las más variadas maniobras para intentar resolverlo, finalmente lo he conseguido siguiendo los siguientes pasos:

1. Desinstalar completamente Python de mi Windows (todas las versiones). También el Python Launcher.
2. Instalar la librería "stockfish" (directamente desde el IDE de PyCharm).
3. Instalar la librería "serial" (directamente desde el IDE de PyCharm).

Luego, al ejecutar el programa ha salido el error

```console

    from serial import Serial
    ImportError: cannot import name 'Serial' from 'serial' (C:\Python\3.10.1\lib\site-packages\serial\__init__.py)

```

Lo que ha quedado resuelto instalando la librería pyserial con


```console

    pip3 install pyserial

```
