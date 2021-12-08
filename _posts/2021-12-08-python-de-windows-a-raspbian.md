---
layout: post
title: De Windows a Raspbian
location: Mora de Rubielos
pygment_theme: native
main_image: /assets/img/raspberry/windows-raspberry-logo1.jpg
---
Ha llegado el momento de migrar de Windows a Raspbian el proyecto ChessPUPython (escrito en Python por si el nombre de jaba alguna duda). Windows nos ha servido para el desarrollo y las pruebas, pero para que el tablero funcione de forma autónoma tenemos que sustituir el PC por una placa Raspberry Pi (en mi caso la Raspberry Pi 2 Model B).

Aprovecho para recordar que ChessPUPython es el progarma que se encarga de intermediar entre la electrónica de Arduino y el motor de juego Stocfish. Como mi esperiencia con Python es más que limitada, he tenido que lidiar con algunas sorpresas al ejecutar ChessPUPython en la Raspeberry, así que he aprovechado para, además de hacer las correciones obligadas, hacer algunas otras mejoras.

Lanzando   

```console

    python main.py

```

me he encontrado estos imprevistos:

##### 1. El juego de caracteres
Parece que no hemos establecido el juego de caracteres

{% assign img_url = "/assets/img/blog/2021-12-08/error-charset.png" %}
{% assign img_description = "" %}
{% assign img_style = "" %}
{% include blog/one-image.html %}

Para solucionarlo solo ha habido que poner como primera línea de nuestro módulo la siguiente:

```python

     # coding=utf-8    

```


##### 2. Librería Python para Stockfish
Aparece este mensaje porque tenemos pendiente instalar la librería que permite a Python trabajar con Stockfish.

{% assign img_url = "/assets/img/blog/2021-12-08/error-stockfish-python-library.png" %}
{% assign img_description = "" %}
{% assign img_style = "" %}
{% include blog/one-image.html %}

Se trata de la que tenemos disponible en [https://pypi.org/project/stockfish/](https://pypi.org/project/stockfish/).

{% assign img_url = "/assets/img/blog/2021-12-08/stockfish-python-library.png" %}
{% assign img_description = "" %}
{% assign img_style = "border: 1px solid #e0e0e0" %}
{% include blog/one-image.html %}

Así que ejecutaremos lo siguiente para instalarla:

```console

    pip install stockfish

```


##### 2. Ruta al ejecutable Stockfish
En la modalidad de Windows teníamos el siguiente código


```python

    ...
    from stockfish import Stockfish
    sf = Stockfish("C:\stockfish_13_win_x64\stockfish_13_win_x64.exe")
    ...

```

Ahora tendremos que cambiarlo por

```python

    ...
    from stockfish import Stockfish
    sf = Stockfish("/usr/games/stockfish")
    ...    

```
