---
layout: post
title: Raspberry. Primera instalación.
location: Mora de Rubielos
pygment_theme: native
main_image: /assets/img/raspberry/logo-raspberry-1.jpg
---
Aunque solo sea para saciar mi curiosidad, voy a tratar de poner en marcha la Raspberry Pi 2. De momento, me conformo con hacerme con los conceptos básicos y conseguir hacerla funcionar, más adelante ya veremos si esta primera instalación es correcta o tenemos que corregirla o rehacerla completamente.

##### 1. Tarjeta SD
Lo primero que tenemos que hacer es conectar a nuestro ordenador el dispositivo USB con la tarjeta SD para poder tener así disponible una nueva unidad de disco y sobre la que haremos la instalación del Sistema Operativo para la Raspberry. En mi caso, la unidad que ha aparecido es la E:.

{% assign img_url = "/assets/img/raspberry/install-usb-sd-pc.jpg" %}
{% assign img_description = "Lector USB para tarjetas SD" %}
{% assign img_style = "max-height: 350px;" %}

{% include blog/one-image.html %}

##### 2. Raspberry Pi Imager
Según la [página oficial de Raspeberry](https://www.raspberrypi.org/), la forma más rápida y fácil de instalar Raspberry Pi OS y otros sistemas operativos en una tarjeta microSD, lista para usar con su Raspberry Pi, es utilizar la aplicación [Raspberry Pi Imager](https://www.raspberrypi.com/software/). Yo al hacerlo he elegido la opción "RASPBERRY PI OS (32-BIT)" y la unidad "E:" que ha aparecido con la conexión de los dispositivos del paso anterior.

{% assign img1_url = "/assets/img/raspberry/raspberry-imager.png" %}
{% assign img1_description = "Rasberry Pi Imager" %}
{% assign img1_style = "max-height: 350px;" %}
{% assign img2_url = "/assets/img/raspberry/imager-install1.png" %}
{% assign img2_description = "Proceso de instalación" %}    
{% assign img2_style = "" %}    
{% include blog/two-images.html %}

La instalación en la SD ha sido bastante rápida y, además, tras las escritura hay un proceso de verificación que garantiza que la información guardada conserva su integridad.

##### 3. Periféricos
Ahora hay que dotar a la placa de los perifédicos básicos para le permitan interactuar con el exterior. Lo primero es introducir la tarjeta SD que hemos preparado en los pasos anteriores en la ranura que se encuentra en la parte posterior de placa. Luego tendremos que conectar alimentación, pantalla, teclado y ratón. los primeros tres he utilizado una conexión HDMI convencional y para los otros dos, dispositivos USB.

{% assign img1_url = "/assets/img/raspberry/connect-sd-1-2.jpg" %}
{% assign img1_description = "Tarjeta SD a la Rasbperry" %}
{% assign img1_style = "max-height: 350px;" %}
{% assign img2_url = "/assets/img/raspberry/raspberry-periferic-2.jpg" %}
{% assign img2_description = "Periféricos fundamentales" %}    
{% assign img2_style = "" %}    
{% include blog/two-images.html %}

1. Fuente de alimentación
2. Conexión HDMI al monitor
3. Teclado USB con cable
4. Ratón USB con cable

##### 3. Arrancando
Una vez esté todo conectado, el sistema arranca y podremos configurar algunas cuestions básicas sobre el idioma, la franja horaria y destalles similares. Respecto al usurio y la contraseña, de momento, para simplificar y en contra las habituales recomendaciones, he dejado el usuario "pi" y la contraseña "raspberry".

{% assign img1_url = "/assets/img/raspberry/background-2.jpg" %}
{% assign img1_description = "Arrancando" %}
{% assign img1_style = "max-height: 350px;" %}
{% assign img2_url = "/assets/img/raspberry/background-1.jpg" %}
{% assign img2_description = "Funcionando" %}    
{% assign img2_style = "" %}    
{% include blog/two-images.html %}

##### 4. Sonido (fracaso total)
Aunque en principio no tengo intención de sacar partido a las capacidades sonoras/musicales de la Raspberry en este proyecto, para asegurarme de que todo lo relacionado con el sonido funciona, he conectado unos pequeños altavoces alimentados por USB. El resultado ha sido un **fracaso total**. Resulta que lo que yo pensaba que era una clásica salida de audio, en realidad es 

{% assign img1_url = "/assets/img/raspberry/speakers-2.jpg" %}
{% assign img1_description = "Minialtavoces" %}
{% assign img1_style = "max-height: 350px;" %}
{% assign img2_url = "/assets/img/raspberry/kk-1.jpg" %}
{% assign img2_description = "Conexión altavoces" %}     
{% assign img2_style = "" %}    
{% include blog/two-images.html %}







##### 3. Conectando
Falta dotar a la placa de conexión a Internet (con cable Ethernet) y de sonido.

##### 3. Actualizando el SO
https://www.raspberrypi.com/documentation/computers/os.html

he utiulizado 
sudo apt update
sudo apt full-upgrade


desactivar modo de ahorro de energía
https://forums.raspberrypi.com/viewtopic.php?t=43932
