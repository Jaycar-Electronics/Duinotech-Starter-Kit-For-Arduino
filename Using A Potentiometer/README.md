# Using a Potentiometer

Use a potentiometer to adjust the brightness of the in-built LED on the Arduino Uno.

![alt text](using-a-potentiometer.png "Using A Potentiometer Circuit")

## Required Kit Components
| Part          | Quantity  	|
| ------------- |:-------------:|
| Potentiometer	| 1 		|
| Jumper Wires	| 6     	|

## Code
```cpp
						// Setting variables which can be easily called to later
int potPin = A0;				// Input pin from the potentiometer
int ledPin = 13;				// Output pin to the LED
int potVal = 0;					// A variable to store the potentiometer value

void setup() {
  pinMode(ledPin, OUTPUT);			// Setting the LED pin as an output	
}

void loop() {
  potVal = analogRead(potPin);			// Setting the potVal variable to the reading from the potPin
  digitalWrite(ledPin, HIGH);			// Turning the LED pin on
  delay(potVal);					// Delay based off the potentiometer value
  digitalWrite(ledPin, LOW);			// Turning the LED pin off
  delay(potVal);					// Delay based off the potentiometer value
}
```
