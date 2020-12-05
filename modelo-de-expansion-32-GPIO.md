---
layout: default
title: Módulo de Expansión 32 GPIO
header_image: composition-1.jpeg
header_text: ChessPU
header_height: 300px
# diferentes estilos de código en http://jwarby.github.io/jekyll-pygments-themes/languages/java.html
---

__Fragmento de código__

***
```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
***

    {% highlight c++ %}
    int ledPin = 13;	// LED que se encuentra en el pin 13
    int n = 0;  	//Entero que contará el paso por la función loop
    void setup() { 
    pinMode(ledPin, OUTPUT);	// El p1n 13 será una salida digital 
    } 
    void loop(){ 
    digitalWrite(ledPin, HIGH);	// Enciende el LED
    delay(1000); 				// Pausa de 1 segundo 
    digitalWrite(ledPin, LOW);		// Apaga el LED 
    n++;					//Incrementamos n
    delay(delayVal(n));			//Pausa de un tiempo variable
    }
 
//Función que devuelve un valor tipo entero según el parámetro pasado

 
int delayVal(int f){
   return f*100;
}
    {% endhighlight %}
***

lieas


{% highlight ruby linenos %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

```ruby
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
```


# Tarjeta Módulo de Expansión 32 GPIO
### Características básicas (tal cual aparecen en Amazon)
Módulos de Expansión IO SPI de Raspberry Pi（Cableado PI API,Chips 74HC595,Entrada y Salida de 8 bits）
32 GPIO Expansion - Esta placa de expansión de cascada soporta 32 GPIO expansión.  
Conexión infinita: el módulo adaptador de extensión IO es capaz de conectar con el mismo módulo infinitamente.  
Cableado PI API & Código de muestra – utiliza cableado PI API y código de muestra.  
Conexión estable - Interfaz SPI garantiza la estabilidad y suavidad de la conexión.  
Entrada de 8 bits y salida – Adopta la entrada serial de 8 bits y salida serial de 8 bits o paralela para hacer la transmisión de datos super estable sin atascarse o cortar.  


<div id="carouselExampleSlidesOnly" class="carousel slide" data-ride="carousel" style="border: 2px solid red;">
  <div class="carousel-inner">
    <div class="carousel-item active d-flex justify-content-center">
        <img src="{{ site.baseurl }}{{ site.imagespath }}components/expansion-32-gpio-1.jpg" class="d-block w-10 img-fluid" style="width: 200px;" alt="...">
    </div>
    <div class="carousel-item justify-content-center">
      <img src="{{ site.baseurl }}{{ site.imagespath }}components/expansion-32-gpio-2.jpg" class="d-block w-10" style="width: 200px;" alt="...">
    </div>
    <div class="carousel-item justify-content-center">
      <img src="{{ site.baseurl }}{{ site.imagespath }}components/expansion-32-gpio-3.jpg" class="d-block w-10" style="width: 200px;" alt="...">
    </div>
  </div>
  <a class="carousel-control-prev" href="#carouselExampleControls" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="carousel-control-next" href="#carouselExampleControls" role="button" data-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>  
</div>