                                                                     26 de Enero de 2022

# Proyecto

En el día de hoy he probado el funcionamiento de un Joystick.

## Resumen

No consiste en mucho, sin más para probar el funcionamiento del Joystick y hacer alguna variación si queremos.

Cabe destacar un dato curioso. El Joystick está formado por dos potenciómetros y un botón.

## Códigos

### Código Joystick

```
const int pinBoton = 3; 
const int pinEjeY = A1; 
const int pinEjeX = A0; 
 
void setup() {
  pinMode(pinBoton, INPUT);
  digitalWrite(pinBoton, HIGH);
  Serial.begin(9600);
}
 
void loop() {
  Serial.print("Boton:  ");
  Serial.print(digitalRead(pinBoton));
  Serial.print("\n");
  Serial.print("Eje X: ");
  Serial.print(analogRead(pinEjeX));
  Serial.print("\n"); //esto es un salto de linea
  Serial.print("Eje Y: ");
  Serial.println(analogRead(pinEjeY));
  Serial.print("\n\n");
  delay(150);
}

```


### Código Joystick con LEDs

```
const int pinBoton = 3; 
const int pinEjeY = A1; 
const int pinEjeX = A0; 
int valorEjeX;
int valorEjeY;
int swichState;

void setup() {
 

 pinMode(6,OUTPUT);
 pinMode(7,OUTPUT);
 pinMode(8,OUTPUT);
 pinMode(9,OUTPUT);
 pinMode(3,INPUT);
 pinMode(pinBoton, INPUT);
 digitalWrite(pinBoton, HIGH);
 Serial.begin(9600);
}

void joystick(){
 
 if (valorEjeX > 512 && valorEjeY < 512) {
   //led 1
   digitalWrite(6,HIGH);
   digitalWrite(7,LOW);
   digitalWrite(8,LOW);
   digitalWrite(9,LOW);
  
 }
 if (valorEjeX < 512 && valorEjeY > 512) {
   //led 2
   digitalWrite(6,LOW);
   digitalWrite(7,HIGH);
   digitalWrite(8,LOW);
   digitalWrite(9,LOW);
 }
   if (valorEjeY < 400 && valorEjeX > 450) {
   //led 3
    digitalWrite(9,HIGH);
   digitalWrite(8,LOW);
  digitalWrite(6,LOW);
   digitalWrite(7,LOW);
 }
 if (valorEjeX < 400 && valorEjeY > 450)
 {
   //led 4
   digitalWrite(8,HIGH);
    digitalWrite(9,LOW);
   digitalWrite(6,LOW);
   digitalWrite(7,LOW);}


}
void loop() {
 valorEjeX = analogRead(pinEjeX);
 valorEjeY = analogRead(pinEjeY);
 swichState = digitalRead(pinBoton);
 Serial.print("Boton:  ");
 Serial.print(swichState);
 Serial.print("\n");
 Serial.print("Eje X: ");
 Serial.print(valorEjeX);
 Serial.print("\n"); //esto es un salto de linea
 Serial.print("Eje Y: ");
 Serial.println(valorEjeY);
 Serial.print("\n\n");
 delay(150);
if (swichState == LOW){
 digitalWrite(6,HIGH);
   digitalWrite(7,HIGH);
   digitalWrite(8,HIGH);
   digitalWrite(9,HIGH);
}
else {
 joystick();
}
 
}

```
