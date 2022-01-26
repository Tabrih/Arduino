                                                        26 de Enero de 2022
                                                        
# Proyecto

Hoy he realizado, junto a [Miguel Ángel](https://github.com/miguelamgel1107) y [David](https://github.com/DavidMenCam), el proyecto de Arduino Cerrojo de Puerta.

## Resumen











## Código

Aquí está el código del proyecto: 

```
#include <Servo.h>
Servo myServo;
const int piezo = A0;
const int switchPin = 2;
const int yellowLed = 3;
const int greenLed = 4;
const int redLed = 5;
int knockVal;
int switchVal;
const int quietKnock = 20;
const int loudKnock = 100;
boolean locked = false;
int numberOfKnocks = 0;
void setup(){
  myServo.attach(9);
  pinMode(yellowLed,OUTPUT);
  pinMode(redLed,OUTPUT);
  pinMode(greenLed,OUTPUT);
  pinMode(switchPin,INPUT);
  Serial.begin(9600);
  digitalWrite(greenLed,HIGH);
  myServo.write(0);
  Serial.println("La caja está abierta");
}
void loop(){
  if(locked == false){
    switchVal = digitalRead(switchPin);
    if(switchVal == HIGH){
      locked = true;
      digitalWrite(greenLed,LOW);
      digitalWrite(redLed,HIGH);
      myServo.write(90);
      Serial.println("La caja está cerrada");
      delay (1000);
    }
  }
  if(locked == true){
    knockVal = analogRead(piezo);
    if(numberOfKnocks < 3 && knockVal > 0){
      if(checkForKnock(knockVal) == true){
        numberOfKnocks++;
      }
      Serial.print(3-numberOfKnocks);
      Serial.println("Moras golpes para ir");
    }
    if(numberOfKnocks >= 3){
      locked = false;
      myServo.write(0);
      delay(20);
      digitalWrite(greenLed,HIGH);
      digitalWrite(redLed,LOW);
      Serial.println("La caja está abierta");
      numberOfKnocks =0;
    }
  }
}
boolean checkForKnock(int value){
  if(value > quietKnock && value < loudKnock){
    digitalWrite(yellowLed,HIGH);
    delay(50);
    digitalWrite(yellowLed,LOW);
    Serial.print("Valor de golpe válido");
    Serial.println(value);
    return true;
  }
  else {
    Serial.print("Valor de golpe no válido");
    Serial.println(value);
    return false;  
  }
}   

```
P.D: En mi caso yo he cambiado el const int quietKnock a 20 ya que me venía mejor, pero de normal es 10.


## Imágenes o Vídeos

Y por último aquí tenéis la imagen y el vídeo del mismo:

![](https://github.com/Tabrih/Arduino/blob/main/Archivos/IMG_20220126_115326.jpg)

[Vídeo del proyecto](https://raw.githubusercontent.com/Tabrih/Arduino/main/Archivos/VID_20220126_115954.mp4)
