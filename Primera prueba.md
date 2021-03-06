
                                                       6 de Octubre de 2021

# Índice

[Arduino](#arduino)

[Protoboard](#protoboard)

[Circuitos Eléctricos](#circuitos-eléctricos)

[Primeros Circuitos](#primeros-circuitos)

[Apuntes sobre electricidad](#apuntes-sobre-electricidad)

[Lenguaje de programación](#lenguaje-de-programación)

[Morse y sus funciones](#morse-y-sus-funciones)

[Errores](#errores)

[Como programar](#como-programar)

[Que hace Blink.ino](#que-hace-blink.ino)

[Snippet](#snippet)




# Arduino

[Apuntes de electricidad](#apuntes-sobre-electricidad)

Primer error de Arduino :

avrdude: ser_open(): can't open device "/dev/ttyACM0": Permission denied

![](https://github.com/Tabrih/Arduino/blob/main/Error%20arduino%201.png)


El error se debe a que no puede acceder al puerto.

### Protoboard 

- Circuito en paralelo

![](https://github.com/Tabrih/Arduino/blob/main/IMG_20211006_123213.jpg)



- Circuito en serie


![](https://github.com/Tabrih/Arduino/blob/main/IMG_20211006_124850.jpg)


![](https://github.com/Tabrih/Arduino/blob/main/IMG_20211006_133654.jpg)



                                                     13 de Octubre de 2021
                                                     
# Circuitos eléctricos

## Error de programación

Intentamos programarl programa de ejemplo blink.ino pero el programa avrdude lanzó una excepción y detuvo el programa. Esto por un tema de permisos de usuario.

![](https://github.com/Tabrih/Arduino/blob/main/Error%20arduino%201.png)



En Linux hay dos tipos de usuario: El usuario y el superusuario.


## Primeros circuitos

### Circuito simple

Este pese a funcionar y dar luz genera dos problemas: 

- Se calienta y es incómodo de tocar

- Puede fundir el LED

### Circuito en serie

Si desconectamos una parte no funciona

### Circuito en paralelo

Da igual si una parte se desconecta
 
### Botones en serie 

![](https://github.com/Tabrih/Arduino/blob/main/IMG_20211006_135736.jpg)



![](https://github.com/Tabrih/Arduino/blob/main/IMG_20211006_135739.jpg)



![](https://github.com/Tabrih/Arduino/blob/main/IMG_20211006_135745.jpg)

Fotos de [Miguel Ángel](https://github.com/miguelamgel1107)

## Apuntes sobre electricidad

Voltaje --> Altura (Diferencia de potencial)

Intensidad o Amperaje --> cantidad de agua o rotuladores

Resistencia --> Resistencia al paso del agua o rotulador

Intensidad = Voltaje ÷ Resistencia ---> Ley de Ohm

Voltaje = Intesidad x Voltaje 

Resistencia = Voltaje ÷ Intensidad

### Por qué necesitamos resistencias con los LEDs?

Tenemos 2 circuitos 

Circuito 1 : 5V,GND 0V

Circuito 2 : 5V, bombilla, GND 0V

El voltaje de los dos circuitos es 5V.

Y la resistencia? Circuito 1, 1 Ohm Circuito 2 440 Ohms

5V ÷ 441 Ohms = 0,01133 A = 11,33 mA

5V ÷ 1 Ohm = 5 A 

5V ÷ 0 Ohm = ∞ A (Cortocircuito) ---> Evitar

## Lenguaje de programación

- Como subir un programa 

- Errores y soluciones

## Morse y sus funciones

[Morse 1](https://github.com/Tabrih/Arduino/blob/main/Morse_1.ino)

[Morse 2](https://github.com/Tabrih/Arduino/blob/main/Morse_2.ino)

[Morse 3](https://github.com/Tabrih/Arduino/blob/main/Morse_3.ino)


                                                        19 de Octubre de 2021


## Errores

El bug es un problema en un programa de un ordenador o software que desencadena un resultado no esperado.

Un glitch es un tipo de bug pero gráfico.

Errores : Está en Runtime Error, Compiling Error

Excepción: Ejemplos Java, Python, Ada.

## Como programar

- Primero tenemos el Arduino IDE instalado.

- Tenemos un usuario con permisos.

- Conectamos el Arduino por USB.

- Cargamos el programa Blink.ino, Archivo --> Ejemplos --> 1. Basics --> Blink

- Pulsamos el botón subir (->) 
 
 Errores posibles --> Si no hay puerto --> Herramientas --> Puerto
 
 Error --> Port busy --> Esperar 1 min aprox sin desenchufar el Arduino
 
 *Conseguimos programar el Blink.ino*
 
 1. Buscarlo en Internet
 
 2. Subirlo Nosotros

 3. Enlazar en primeras pruebas.md

Después de blink.ino iniciamos pruebas en código morse

Morse 1 --> Hicimos modificaciones en el código para cambiar el tiempo de brillo. Para eso hicimos cambios en de lineas de delay (_);

# Que hace Blink.ino

void loop () {

Cuatro sentencias ( o líneas)

}

- digitalWrite(LED_BUILTIN, HIGH);

- delay (1000)

- digitalWrite(LED_BUILTIN, LOW);

- delay (1000)

delay (_) --> nos pide un número, ese número será los milisegundos de espera

1000 --> 1 segundo

60000 --> 1 minuto

500 --> medio segundo

50 = 0,05 s --> el ojo humano no lo ve

- Hicimos un pulso largo y un pulso corto

Pulso largo de 200 500 y pulso corto de 100 300

#### Snippet

Un Snippet fragmento de código que no funciona por sí mismo que sirve para una función concreta.

Los snippets se copian, se pegan y, normalmente, se adaptan al código a mano por le programadore.
