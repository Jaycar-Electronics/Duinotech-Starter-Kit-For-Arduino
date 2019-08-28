# Fan Speed Controller

Use variable feedback from a potentiometer to adjust the speed of the motor.

![alt text](fan-speed-controller.png "Fan Speed Controller Circuit")

## Required Kit Components
| Part          | Quantity  	|
| ------------- |:-------------:|
| Potentiometer	| 1 		|
| Motor		| 1		|
| Jumper Wires	| 5     	|

## Code
```cpp										
												// Setting variables which can be easily called to later
int POT_PIN = A0;				// Input pin from the potentiometer
int MOTOR_PIN = 9;				// Output pin to the motor
int motorSpeed = 0;				// Setting a variable to store the resulting motor speed value
int potVal = 0;						// Setting a variable to store the resulting potentiometer value

void setup()				// Runs once when sketch starts
{
  pinMode(MOTOR_PIN, OUTPUT);		// Setting the pin type & defining the I/O
}

void loop()					// Runs repeatedly
{
  potVal = analogRead(POT_PIN);			// Setting the potVal variable to the reading from the POT_PIN (potentiometer input pin)

  motorSpeed = map(potVal, 0, 1023, 0, 255);		// Setting the motorSpeed variable to an equivalent variable between 0 & 255, based off the potVal which is between 0 & 1023

  analogWrite(MOTOR_PIN, motorSpeed);		// Writing the mapped value to the motorSpeed pin
}
```
