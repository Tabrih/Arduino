
                                                  30 de Noviembre de 2021


En el día de hoy vamos a abrir una funcionalidad a un proyecto anterior. En el grupo estoy con [Stiven](https://github.com/St1v3n3223) y vamos a hacer el proyecto Medidor de amor.

A este proyecto le vamos a añadir un botón que lo apague y lo encienda.

# Código

```C++

const int sensorPin = A0;
const float baselineTemp = 20.0;

int switchState = 0;
bool isTheButtonBeingPressed = false;
bool play = false;

int buttonPin = 5;
void setup(){
  Serial.begin (9600);
  for( int pinNumber = 2; pinNumber<5 ; pinNumber++){
    pinMode(pinNumber, OUTPUT);
    digitalWrite (pinNumber, LOW);
  pinMode(buttonPin, INPUT);
  }
}
 

void loop (){
  checkButton();
  if (play) {
mirarAmor();
  }
  else{
    apagarLuces();
  }
}

void apagarLuces() {
     digitalWrite (2, LOW);
    digitalWrite (3, LOW);
    digitalWrite (4, LOW);
}

void checkButton(){
  switchState = digitalRead(buttonPin);
  if (switchState == HIGH && !isTheButtonBeingPressed){
    play = !play;
    isTheButtonBeingPressed = true;
  }
  
  if (switchState == LOW)
  {
  isTheButtonBeingPressed = false;
  }

}
  void mirarAmor(){
 
  int sensorVal = analogRead (sensorPin);

  Serial.print("Sensor Value: ");
  Serial.print(sensorVal);


  float voltage = (sensorVal/1024.0) * 5.0;

  Serial.print (" , Volts: ");
  Serial.print(voltage);

  Serial.print(" , degrees C: ");

  float temperature = (voltage - .5) * 100;

  Serial.println(temperature);

  if(temperature < baselineTemp){

    digitalWrite (2, LOW);
    digitalWrite (3, LOW);
    digitalWrite (4, LOW);
    
  }else if(temperature >= baselineTemp+2 && temperature < baselineTemp+4) {
  digitalWrite(2, HIGH);
  digitalWrite(3, LOW);
  digitalWrite(4, LOW);

  }else if(temperature >= baselineTemp+4 && temperature < baselineTemp+6) {
  digitalWrite(2, HIGH);
  digitalWrite(3, HIGH);
  digitalWrite(4, LOW);

}else if(temperature >= baselineTemp+6){
  digitalWrite(2, HIGH);
  digitalWrite(3, HIGH);
  digitalWrite(4, HIGH);


  }

  delay(1);

  }
```
