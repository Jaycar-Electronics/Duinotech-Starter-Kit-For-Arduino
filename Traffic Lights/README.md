# Traffic Lights

Simulate traffic lights using multiple LEDs & a loop circuit in Arduino.

![alt text](traffic-lights.png "Traffic Light Circuit")

## Required Kit Components
| Part          | Quantity  		|
| ------------- |:---------------------:|
| LEDs		| 3 (green/red/yellow)	|
| Resistors	| 3			|
| Jumper Wires	| 4     		|

## Code
```cpp
						// Setting variables which can be easily called to later
int GREEN = 2;			// Setting the pins from the LEDs
int YELLOW = 3;
int RED = 4;
int DELAY_GREEN = 5000;		// Setting variables for delays that can be adjusted
int DELAY_YELLOW = 2000;	// without altering each function
int DELAY_RED = 5000;

void setup()					// Runs once when sketch starts
{
  pinMode(GREEN, OUTPUT);		// Setting the LEDs to outputs
  pinMode(YELLOW, OUTPUT);
  pinMode(RED, OUTPUT);
}

void loop()					// Runs repeatedly
{
  green_light();
  delay(DELAY_GREEN);
  yellow_light();
  delay(DELAY_YELLOW);
  red_light();
  delay(DELAY_RED);
}

void green_light()				// A function for turning only the green LED on
{
  digitalWrite(GREEN, HIGH);	// Turning on the green LED & the others off
  digitalWrite(YELLOW, LOW);
  digitalWrite(RED, LOW);
}

void yellow_light()				// A function for turning only the yellow LED on
{
  digitalWrite(GREEN, LOW);		// Turning on the yellow LED & the others off
  digitalWrite(YELLOW, HIGH);
  digitalWrite(RED, LOW);
}

void red_light()				// A function for turning only the red LED on
{
  digitalWrite(GREEN, LOW);		// Turning on the red LED & the others off
  digitalWrite(YELLOW, LOW);
  digitalWrite(RED, HIGH);
}
```
