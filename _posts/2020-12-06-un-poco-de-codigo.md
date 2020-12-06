---
layout: post
title:  Un poco de código
permalink: /blog/:day-:month-:year/un-poco-de-codigo.html
location: Mora de Rubielos
pygment_theme: native
---
El único objetivo de la entrada de hoy es conservar el código de Arduino que he utilizado
en la gestión en serie de los chips 74HC595 para controlar los leds del tablero. 

Como he realizado bastantes ensayos con diferentes códigos y librerías, prefiero
conservar ya esta muestra de código, antes de que se me traspapele.


```c++

    /*
    ShiftRegister74HC595 - Library for simplified control of 74HC595 shift registers.
    Developed and maintained by Timo Denk and contributers, since Nov 2014.
    Additional information is available at https://timodenk.com/blog/shift-register-arduino-library/
    Released into the public domain.
    */

    #include <ShiftRegister74HC595.h>

    // create a global shift register object
    // parameters: <number of shift registers> (data pin, clock pin, latch pin)    
    ShiftRegister74HC595<4> sr(2, 3, 4);
 
    void setup() { 
        Serial.begin(9600); // open the serial port at 9600 bps:
    }

    void loop() {
        // setting all pins at the same time to either HIGH or LOW
        Serial.println("TODOS");
        sr.setAllHigh(); // set all pins HIGH
        delay(100);

        Serial.println("NINGUNO");
        sr.setAllLow(); // set all pins LOW
        delay(100); 
        
        Serial.println("UNO A UNO");
        // setting single pins
        for (int i = 0; i < 32; i++) {
            Serial.print("PIN ");
            Serial.println(i);  
            sr.set(i, HIGH); // set single pin HIGH
            delay(50); 
        }
    }

```
Por lo demás, otro día de frío intenso en el que Dana y yo hemos ido por la mañana a Virgen de la Vega a pasear un poco. Lamentablemente, mi estado emocional no ha sido como el de ayer, un día del que disfruté mejorando el blog y dándole contenido. Por la mañana he cumplido con mis obligaciones, pero al volver del paseo todo ha cambiado y la tormenta interior ha vuelto.

Pero no hay otra opción que afrontar la lucha interior y convertir en maestra la instrospección constante a la que obliga esta extraña soledad elegida.

{% assign img_url = "/assets/img/personal/vega3.jpg" %}
{% assign img_description = "Humilladero de Virgen de la Vega / Alcalá de la Selva" %}
{% include blog/one-image.html %}