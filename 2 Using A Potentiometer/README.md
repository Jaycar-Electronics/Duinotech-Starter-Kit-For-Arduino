# Using a Potentiometer

Use a potentiometer to adjust the brightness of the in-built LED on the Arduino Uno.

This extends the previous project:

1. Change the LED connection from pin 13 to pin 9.
2. Connect the potentiometer to the circuit as below.

![alt text](using-a-potentiometer.png 'Using A Potentiometer Circuit')

## Required Kit Components

| Part          | Quantity |
| ------------- | :------: |
| Potentiometer |    1     |
| Jumper Wires  |    6     |

## Code

```cpp
int potPin = A0;        // Input pin from the potentiometer
int ledPin = 9;        // Output pin to the LED
int potVal = 0;          // A variable to store the potentiometer value
int brightness = 0;

void setup()          // Runs once when sketch start
{
  pinMode(ledPin, OUTPUT);      // Setting the LED pin as an output
}

void loop()          // Runs repeatedly
{
  //read from the pot pin, and store it into potval
  potVal = analogRead(potPin);

  //"map" the brightness, so that potval (0->1023)
  // corresponds with a value between (0->255)

  brightness = map(potVal , 0, 1023, 0, 255);

  //analog write uses PWM to control the brightness of the LED.
  // it will only work on the PWM pins, which pin 9 is.
  analogWrite(ledPin, brightness);
}
```
