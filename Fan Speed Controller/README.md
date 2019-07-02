# Fan Speed Controller

![alt text](fan-speed-controller.png "Fan Speed Controller Circuit")

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
