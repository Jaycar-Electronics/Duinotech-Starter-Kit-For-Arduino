# Using a Potentiometer

Use a potentiometer to adjust the brightness of the in-built LED on the Arduino Uno.

![alt text](using-a-potentiometer.png "Using A Potentiometer Circuit")

## Required Kit Components
| Part          | Quantity  	|
| ------------- |:-------------:|
| Potentiometer	| 1 		|
| Jumper Wires	| 6     	|

## Code
```
int sensorPin = A0;
int ledPin = 13;
int sensorValue = 0;

void setup() {
  pinMode(ledPin, OUTPUT);
}

void loop() {
  sensorValue = analogRead(sensorPin);
  digitalWrite(ledPin, HIGH);
  delay(sensorValue);
  digitalWrite(ledPin, LOW);
  delay(sensorValue);
}
```
