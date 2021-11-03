
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
