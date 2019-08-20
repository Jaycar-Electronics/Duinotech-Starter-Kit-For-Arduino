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
```
const int POT_PIN = A0;
const int MOTOR_PIN = 9;
int motorSpeed = 0;
int potVal = 0;

void setup()
{
  pinMode(MOTOR_PIN, OUTPUT);
}

void loop()
{
  potVal = analogRead(POT_PIN);

  motorSpeed = map(potVal, 0, 1023, 0, 255);

  analogWrite(MOTOR_PIN, motorSpeed);
}
```
