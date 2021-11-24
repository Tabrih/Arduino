
                                              24 de Noviembre de 2021
                                              
Hoy junto a [David](https://github.com/DavidMenCam) y [Miguel Ángel](https://github.com/miguelamgel1107) he realizado el proyecto Theremin Óptico                                              
# Resumen

- En tu protoboard, conecta las líneas de bus exteriores a la corriente y a la toma de tierra.
- Toma el piezo, y conecta a un lado a la toma de tierra, y el otro a la clavija digital 8 en el Arduino.
- Coloca un fototransistor en la placa de prototipado, conectado el terminal ms largo a 5V. Conecta el otro terminal al pin analógico de Arduino, y a tierra a través de una resistencia de 10 kilo Ohmios.




## Introducción teórica
Un Theremin es un instrumento que genera sonidos mediante el movimiento de las manos de un músico alrededor de este instrumento. Probablemente habrá oído alguno de ellos en películas de terror. El Theremin detecta donde se produce el movimiento de la mano del artista en relación a dos antenas al poder leer la variación de la carga capacitiva de estas antenas. Las antenas se conectan a un circuito analógico que crea los sonidos. Una de las antenas controla la frecuencia del sonido y la otra controla el volumen. Aunque Arduino no puede producir de una forma exacta los misteriosos sonidos de este instrumento, si que es posible emularlos usando la función tone(). La figura 1 muestra los diferentes tonos que se producen al usar analogwrite() y tone(). Esto posibilita que un transductor como pueda ser un altavoz o un zumbador se mueva hacia delante y hacia atrás a diferentes velocidades.

