                                                     26 de Enero de 2022
                                                            
# Proyecto

En el día de hoy, junto a [David](https://github.com/DavidMenCam) y [Miguel Ángel](https://github.com/miguelamgel1107), he realizado el proyecto de Arduino llamado Lámpara táctil.

## Resumen


## Código

Aquí está el código de este proyecto:

```
#include <CapacitiveSensor.h>
CapacitiveSensor capSensor = CapacitiveSensor(4,2);
int threshold = 1000;
const int ledPin = 12;

void setup() {
  Serial.begin(9600);
  pinMode(ledPin, OUTPUT);
}
void loop() {
  long sensorValue = capSensor.capacitiveSensor(30);
  Serial.println(sensorValue);
  if(sensorValue > threshold) {
    digitalWrite(ledPin, HIGH);
  }
  else {
    digitalWrite(ledPin, LOW);
  }
  delay(10);
}

```

## Imágenes o Vídeos

Aquí se encuentra la imagen y vídeo del proyecto:

![](https://github.com/Tabrih/Arduino/blob/main/Archivos/IMG_20220126_131142.jpg)

[Vídeo de la Lámpara Táctil](https://raw.githubusercontent.com/Tabrih/Arduino/main/Archivos/VID_20220126_131329.mp4)
