# Using Buttons
![alt text](button-buzz.png "Using Buttons Circuit")

## Required Kit Components
| Part          | Quantity  	|
| ------------- |:-------------:|
| Switch	| 1 		|
| Buzzer	| 1		|
| Jumper Wires	| 7     	|

## Code
```
  int Button = 7;
  int Buzzer = 11;
  int Val = 0;

void setup()
{
  pinMode(Button, INPUT_PULLUP);
  pinMode(Buzzer, OUTPUT);
}

void loop()
{
  Val = digitalRead(Button);
  if (Val == LOW) {
    digitalWrite(Buzzer, HIGH);
  } else {
    digitalWrite(Buzzer, LOW);
  }
}
```
