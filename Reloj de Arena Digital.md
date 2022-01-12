                                                          12 de Enero de 2022 
                                                          
# Proyecto 

Hoy junto a [Miguel Ángel](https://github.com/miguelamgel1107) he realizado el proyecto de Arduino llamado Reloj de Arena Digital.

## Introducción teórica

### Delay y sus problemas

Cuando el Arduino invoca delay(), congela su estado actual durante la duración del mismo. Esto se refiere a que no puede haber ninguna entrada o salida mientras espera. No son útiles para llevar una cuenta del tiempo. Si por algún casual quiseras hacer algo cada 10 segundos, tener 10 segundos de delay sería una pesadez.

### Millis() y lo que hará

La función Millis() ayuda a resolver los problemas que causa delay(). Lleva cuenta del tiempo durante el que nuestro Arduino ha estado funcionando en milisegundos.


### Tipo int y tigo long como variable

Ambos, tanto tipo int como tipo long sirven para almacenar tiempo. La diferencia es que tipo int puede tener valores entre -32.768 y 32.767, mientras que tipo long puede llegar hasta 4.294.967.295.


### Tilt sensor

Tilt sensor o mejor llamado interruptor de inclinación en un sensor de encendido y apagado,igual que un interruptor común. En este caso se usará como entrada digital. Lo que los hace diferentes es que detectan la orientación, con una pequeña bola metálica que contienen en su interior y, al este inclinarse de cierta manera, la bola rueda a un lado del pequeño agujero del interruptor y conecta los dos contactos en nuestra protoboard, cerrando el interruptor.






## Montaje
- Foto
- Código (Enlace Código)
