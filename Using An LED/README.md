# Using an LED

This basic project will introduce the beginner Arduino user to simple code & circuits by turning on & off an LED.

![alt text](LED.png "Using An LED Circuit")

## Required Kit Components
| Part          | Quantity  	|
| ------------- |:-------------:|
| LED		| 1 		|
| Resistor	| 1		|
| Jumper Wires	| 2     	|

## Code
```
void setup() {
  pinMode(13, OUTPUT);
}
void loop() {
  digitalWrite(13, HIGH);   
  delay(1000);              
  digitalWrite(13, LOW);   
  delay(1000);             
}
```
