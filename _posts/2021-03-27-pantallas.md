---
layout: post
title:  Pantallas
permalink: /blog/:day-:month-:year/pantallas.html
location: Mora de Rubielos
pygment_theme: default
main_image: /assets/img/misc/screens/lcd24x10.png
---
He probado tres opciones para dotar al tablero de pantalla. Ordenadas de menos artenal a más, son las siguientes:


#### Opción 1. Pantalla LCD de 20x4
---
En concreto se trata del producto IIC I2C Serial LCD Screen 2004 20X4 Modulo Display LCD 2004/20 x 4, 5V para Arduino Uno R3 MEGA 2560
([Amazon](https://www.amazon.es/gp/product/B082R7RPZX/ref=ppx_yo_dt_b_asin_title_o01_s00?ie=UTF8&psc=1)).

{% assign img_url = "/assets/img/misc/screens/lcd24x10.png" %}
{% assign img_style = "max-height: 300px;" %}
{% assign img_description = "IIC I2C Serial LCD Screen 2004 20X4" %}
{% include blog/one-image.html %}

Ha funcionado de maravilla. He empleado el código disponible en esta [página ](https://www.taloselectronics.com/blogs/tutoriales/lcd-20-x-4-con-luz-de-fondo-azul-con-interfaz-i2c) que emplea esta [librería](https://github.com/TalosElectronics1/LCD-20x4-con-interfaz-I2C).

Solo **he tenido que solucionar un problema** a nivel de código. Resulta que una vez instalada la librería, al compilar me salía el siguiente error:

```
C:\Users\Juan Carlos\Documents\Arduino\libraries\LiquidCrystal\I2CIO.cpp:35:10: fatal error: ../Wire/Wire.h: No such file or directory
 #include <../Wire/Wire.h>
          ^~~~~~~~~~~~~~~~
compilation terminated.
exit status 1
Error compilando para la tarjeta Arduino Uno.

```

Lo he solucionado editando el fichero I2CIO.cpp que se indica en el error y sustituyendo

```c++
    #include <../Wire/Wire.h>
```
por
```c++
    #include <Wire.h>
```

#### Opción 2. Pantalla LCD de 16x2 con adaptador
---
Con el adaptador de interfaz que venía independiente en el kit de la imagen de arriba, se puede gestionar una pantalla LCD de 16x2 cambiando simplemente los parámetros del código del programa de la opción 1 poniendo lo siguiente:

```c++

 lcd.begin(10, 2);//Inicializar la LCD 10x2

```

Funciona todo perfectamente

{% assign img_url = "/assets/img/misc/screens/lc16x2-con-interfaz.jpeg" %}
{% assign img_style = "max-height: 400px;" %}
{% assign img_description = "" %}
{% include blog/one-image.html %}


#### Opción 3. Pantalla LCD de 16x2 con Shift Register 74HC595
---
Es la más artenasal pero es a la que me gustaría recurrir, ya que ya tengo el chip y el potenciómetro instalados en el tablero. La
idea es emplear la librería LiquidCrystal_74HC595.




