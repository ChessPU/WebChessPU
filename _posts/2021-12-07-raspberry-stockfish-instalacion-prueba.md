---
layout: post
title: Stockfish en Raspberry Pi.
location: Mora de Rubielos
pygment_theme: native
main_image: /assets/img/blog/2021-12-07/header.png
---
##### Instalación
He perdido mucho tiempo con innecesarios e infructuosos intentos de compilación de Stockfish en la Raspberry Pi 2. Estaba convencido de que la compilación manual era la única vía para instalarlo en Raspbian, pero, para mi sorpresa, la instalación solo requería una instrucción desde consola:

```console

    sudo apt-get install stockfish

```

        {% assign img_url = "/assets/img/blog/2021-12-07/raspberry-stockfish-installation.jpg" %}
        {% assign img_description = "Instalación de Stockfish en Raspberry Pi 2" %}
        {% assign img_style = "" %}

        {% include blog/one-image.html %}

Una vez hecho esto, tecleando
```console

    stockfish

```
el motor de ajedrez se ha ejecutado a la primera y sin contratiempos. Para comprobarlo, he lanzado el comando "d" con total éxito:

        {% assign img_url = "/assets/img/stockfish/stockfish-running-on-raspberry.png" %}
        {% assign img_description = "Stockfish corriendo en Raspberry Pi 2" %}
        {% assign img_style = "" %}

        {% include blog/one-image.html %}


##### Ubicación
Una vez concluida la instalación, editando el fichero
```console

    vi /var/lib/dpkg/info/stockfish.list

```
podemos conocer la ubicacion de los componentes de Stockfish. Concretamente, el ejecutable queda en
```console

    /usr/games/stockfish

```