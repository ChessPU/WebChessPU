---
layout: default
title: Shift Register 74HC595
header_image: chips/composition-74HC595-1.jpeg
header_text: Shift Register 74HC595
header_height: 300px
# diferentes estilos de código en http://jwarby.github.io/jekyll-pygments-themes/languages/java.html
---
Un problema habitual al trabajar con Arduino es la escasez de pines. Cuando 
nuestro proyecto alcanza cierta complejidad y necesitamos controlar un número 
elevado de dispositivos, nos encontramos con que la cantidad de pines de la placa se nos 
queda corta.

Para romper con esta limitación, existen chips como el 74HC595. Es muy 
económico (yo los he comprado a 0,59 € la unidad) y **nos permite convertir
3 pines de salida de nuestra placa Arduino, en 8**. Además, como los 
74HC595 se pueden conectar en cascada, esos tres pines iniciales podríamos
perfectamente convertirlos en 32 utilizando solamente 4 chips.

Aquí no vamos a hacer un análisis profundo del funcionamiento de este chip, 
sino sencillamente dar unas nociones muy básicas para ser capaces de manejarlo
sin tener que entender la "magia" que tiene lugar en su interior.

En cualquier caso, para aquellos que estén interesados en los detalles técnicos de 
bajo nivel, aquí está su [Data Sheet]({{ site.assetspath }}/pdf/74HC595-data-sheet.pdf){:target="_blank"}.  

## Pines

---
No nos tenemos que preocupar demasiado si no entendemos la breve descripción de los pines que se hace a continuación.
En primer lugar, éstas no proporcionan información suficiente para entender el funcionamiento del chip, y en segundo lugar y más importante, **los pines "complicados" (DS, STCP y SHCP) los gestionaremos con una librería de Arduino** que se encargará del trabajo duro.

{% assign img_url = "/assets/img/chips/74HC595-chip-1.png" %}
{% assign img_description = "Chip 74HC595" %}
{% assign img_style = "max-height: 1000px;" %}
{% include page/one-image.html %}


- **Vcc**  
Alimentación (hasta un máximo de 6 o 7 voltios dependiendo del modelo). Lo habitual es utilizar 5V.

- **GND**  
Toma de tierra

- **Q0...Q7**  
Salidas de datos en paralelo

- **DS**  
Entrada de datos en serie. Este es el pin al que se envían los datos, en función de los cuales se controlan las 8 salidas.

- **OE (Output Enable)**  
Se utiliza para apagar las salidas. Debe mantenerse a cero para un funcionamiento normal, por lo que lo tendremos conectado a GND.

- **STCP (Latch)**  
Se utiliza para actualizar los pines de salida del pin. Los escribe y los mantiene hasta que se reciben nuevos datos.

- **SHCP (Clock Pin)**  
Indica cuándo hay que leer el bit que entra por DS.

- **MR (Master Reset)**  
Restablece todas las salidas a 0. Debe mantenerse en 1 para un funcionamiento normal, por lo que lo tendremos conectado a Vcc.

- **Q7S (también llamado Q7')**  
Salida serie (se utiliza para las conexiones en cascada)