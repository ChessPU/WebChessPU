---
layout: post
title:  El reinicio
permalink: /blog/:day-:month-:year/el-reinicio.html
location: Mora de Rubielos
---
Sábado frío en Mora de Rubielos. Tan frío que lo mejor es quedarse en casa 
calentito y tratar de disfrutar un poco de cosas como el intelecto, la creatividad y la 
lectura. Así que, finalizadas las inevitables tareas caseras y caninas (atender a mi
querida perra Dana), me he metido en mi despachito para devolver a **chessPU** a la vida. 

{% assign img_url = "/assets/img/personal/mora-development-desk-2020-12-05.jpeg" %}
{% assign img_description = "Mi pequeño despacho en Mora de Rubielos" %}
{% include blog/one-image.html %}

No sé si esta resurrección será definitiva, pero la cuestión es que, después de
semanas de abandono, por fin he decidido retomar el proyecto. La razón del parón 
no ha sido otra que la dificultad en reconocer que me encuentraba en un callejón 
sin salida; que no hay más remedio que deshacer lo andado para reconducir el 
proyecto y hacerlo viable.

La falta de planificación y la impaciencia por pasar a la acción sin pensar
demasiado en las consecuencias, han convertido el tablero en un verdadero infierno. La
parte posterior es una inmanejable maraña de cables 
enormes (en grosor y longitud), y las placas montadas en los laterales con 
los circuitos integrados han resultado ser terriblemente incómodas.


{% assign img1_url = "/assets/img/misc/kaos-1.jpeg" %}
{% assign img1_description = "Imposible trabajar bajo estos cables" %}
{% assign img2_url = "/assets/img/misc/kaos-2.jpeg" %}
{% assign img2_description = "Placa y tablero de este modo impiden cualquier tarea" %}
{% include blog/two-images.html %}

Cualquier maniobra para hacer una verificación, reparar una conexión o, mucho peor,
girar al tablero para dejarlo en la que será su posición normal de juego, 
se han vuelto imposibles. Al final se han traducido siempre en una nueva avería 
misteriosa, otra desconexión o el desperfecto más inopinado.

Para colmo, las placas que pretendían ser el interfaz de conexiones con el 
exterior (Arduino, Raspberry, etc.), tienen fallos de conexión constantes y 
los propios conectores se han acabado desprendiendo.

{% assign img1_url = "/assets/img/misc/kaos-3.jpeg" %}
{% assign img1_description = "Las conexiones a la placas de interfaz se sueltan" %}
{% assign img2_url = "/assets/img/misc/kaos-4.jpeg" %}
{% assign img2_description = "Los conectores se desprenden" %}
{% include blog/two-images.html %}

En definitiva, un **desastre sin paliativos**. No queda otra que desmontar y hacer
las cosas de otra manera. 
<br><br>

---

### El plan de reconducción

---

Para no volver a caer en la improvisación, ahora 
voy a seguir un pequeño plan organizado. Además, así se me hace más llevadero; 
se reduce la sensación de derrota.

- **Desoldar del tablero los cables provenientes de las placas que tienen los chips 74HC595**<br>
Tras esta operación, quedarán por un lado las placas con los 74HC595 y los cables, y por otro el tablero ya liberado.

- **Cambiar completamente la filosofía de cableado**<br>
Emplear cables Dupont pegados al tablero y bien organizados que no cuelguen ni impidan
trabajar. La futura instalación de los sensores para las piezas tiene que poder
hacerse son facilidad y sin provocar desperfectos en la circuitería que
gestiona los leds.

- **Nuevas placas con 74HC595 en serie**<br>
Renuncio a las plaquitas que hice a mano con los 74HC595, para utilizar otras ya montadas, 
que son mucho más pequeñas y tienen los conectores preparados.

{% assign img_url = "/assets/img/components/expansion-32-gpio-1.jpg" %}
{% assign img_description = "Módulo de expansión 32 GPIO" %}
{% assign img_style = "max-height: 200px;" %}
{% include blog/one-image.html %}

- **Fijar lo módulos de expansión**<br>
La idea es montar las nuevas plaquitas en el lateral del tablero, aunque en este momento todavía no tengo muy claro cómo.

