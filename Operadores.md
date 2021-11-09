
                                          3 de Noviembre de 2021
                                          
                                                                                   
# Operaciones

IF (Variable y valor fijo), Si (True), No (False)

Output -> Stiven actívate 

EJEMPLO :

Temperatura (15 ºC - 80 ºC)

Sensor Value (0 - 1024)

Se puede encadenar infinitas veces

- Leer Pinao -> Analog Read -> 0 - 1023 (8 bytes)

- Transforma los valores y, de regalo, las pinta en pantalla.

- Decidir 

Digital Write es una función que nos pide un número de pin y el valor HIGH(1) o LOW(0). Si el valor es HIGH, la placa suministrará 5 Voltios en ese pin. Si el valor es LOW, la placa suministrará 0 voltios en ese pin. Si hay 5 voltios, se activarán los circuitos* Si es 0V no se activarán.

* Depende del hardware y como esté conectado.

} else if ( temperature >= baselineTemp+2 && temperature < baselineTemp+4){

digitalWrite(2,HIGH),

digitalWrite(3,LOW),

digitalWrite(4,LOW),


} else if ( temperature >= baselineTemp+4 && temperature < baselineTemp+6){

digitalWrite(2,HIGH),

digitalWrite(3,HIGH),

digitalWrite(4,LOW),

} else if ( temperature >= baselineTemp+4)

digitalWrite(2,HIGH),

digitalWrite(3,HIGH),

digitalWrite(4,HIGH),

- Ejercicio : 

Vamos a conectar 2 botones y 2 LEDs

Haremos diferentes programas con diferentes comportamientos

Para poner un botón necesitamos una resistencia de 10000 Ω Ohmnios. Estas son las que tienen cuerpo beige y una línea naranaja.

Pin ___ Pulsador___ GND (Grand)                                                                                                                      

       //

5V____ Resistencia 10k Ohmnios

Esquema de botón " Por defecto arriba" o "Pulled High"

Conectaremos 2 botones. Uno al pin 2 y otro al pin 3. Para poner un LED necesitamos una resistencia de 220 Ω Ohmnios, las de cuerpo azul. Hay que tener en cuenta la polaridad del led. La pata más corta va a hacia el GND(0V) y la larga hacia el voltaje.

PIN -->---///---GND                                                                                                                     

     LED 220Ω

Da igual si la resistencia va detrás o delante del LED. Conectaremos 2 LEDS, una al pin 4 y otra al pin 5.

 ### Arduino 

 * Versión 1

 Hemos comenzado copiando unos códigos en la pizarra de la versión uno la cual seria esta en particular 

 [Versión 1 y principal](https://github.com/DavidMenCam/Arduino/tree/main/Arduino%20%20version%201)

 * Versión 2

 En la segunda versión hemos hecho que parpadease siempre  cuando le dabamos a un botón se encendía otro y al contrario.

 [Versión 2](https://github.com/DavidMenCam/Arduino/blob/main/arduino%20version%202/albedo_god_2.ino)

 * Versión 3

 Lo que hemos hecho en la versión 3 es que siempre estén parpadeando sin parar y cuando le das a un botón se enciende uno y cuando le das a otro se enciende otro 

 [Versión 3](https://github.com/DavidMenCam/Arduino/blob/main/Arduino%20version%203/albedo_god_3.ino)

 * Versión 4

 En la versión 4 siempre estaban apagados y se encendían con cualquiera de los dos botones 

 [Versión 4](https://github.com/DavidMenCam/Arduino/blob/main/arduino_ver_4/arduino_ver_4.ino)

 * Versión 5

 En la versión 5 siempre están parpadeando permanentemente, cuando aprietas el botón que está conectado al pin dos brilla el LED del pin 4 y el otro LED se apaga , cuando el botón que está conectado al pin 3 se aprieta, se enciende el LED que está conectado al pin 5 y el otro led se apaga y, si oprimes los dos botones, los dos LEDS se mantienen encendidos 

 [Versión 5](https://github.com/DavidMenCam/Arduino/blob/main/arduino_ver_5/arduino_ver_5.ino)

 * Versión 6

 Usamos este operador (!) este sirve para hacer la acción contraria de lo que se desea 

 [Versión 6](https://github.com/DavidMenCam/Arduino/tree/main/arduino_ver_6)

 * Versión 7

  Lo que hicimos en el último fue una variante de colores en cada LED haciendo que cada uno tuviera un color diferente

 [Versión 7](https://github.com/DavidMenCam/Arduino/blob/main/arduino_ver_7.ino)

 Versión 7.2, hemos cambiado los LEDS por reguladores aunque la mecánica funciona, el LED verde no sufre efecto y ni se ve el color, lo arreglaremos junto a David  el martes 

![](https://github.com/miguelamgel1107/Arduino/blob/main/IMG20211103140539.jpg)
