Sequential LED Blink

Overview:
This project demonstrates a simple sequential LED blinking pattern using an Arduino. The program turns on and off seven LEDs connected to the Arduino's pins, with each LED staying on for 2 seconds before moving to the next. After completing the sequence, it reverses the process and starts blinking again.

Hardware Requirements:
- 1x Arduino Board (e.g., Arduino Uno)
- 7x LEDs
- 7x Resistors (220 ohms or 330 ohms)
- Jumper wires
- Breadboard (optional)

Circuit Setup:
1. Connect 7 LEDs to Arduino pins 2, 3, 4, 5, 6, and 7 (for this example).
2. Each LED should have a current-limiting resistor (220Ω) connected to its ground (GND) leg.
3. The anode (long leg) of each LED should be connected to the respective pin on the Arduino.

Code Explanation:
- The `setup()` function configures Arduino pins 2 to 7 as **OUTPUT**.
- In the `loop()`, each LED is turned **ON** for 2 seconds, then turned **OFF**, and the sequence repeats.
- After the LEDs complete the sequence, they are turned on in reverse order, starting from pin 6 to 2.

void setup() {
  // Set the pins 2 to 7 as OUTPUT for LEDs
  pinMode(2,OUTPUT);
  pinMode(3,OUTPUT);
  pinMode(4,OUTPUT);
  pinMode(5,OUTPUT);
  pinMode(6,OUTPUT);
  pinMode(7,OUTPUT);
}

void loop() {
  // Blink LEDs sequentially
  digitalWrite(2,HIGH);
  delay(2000);
  digitalWrite(2,LOW);
  digitalWrite(3,HIGH);
  delay(2000);
  digitalWrite(3,LOW);
  digitalWrite(4,HIGH);
  delay(2000);
  digitalWrite(4,LOW);
  digitalWrite(5,HIGH);
  delay(2000);
  digitalWrite(5,LOW);
  digitalWrite(6,HIGH);
  delay(2000);
  digitalWrite(6,LOW);
  digitalWrite(7,HIGH);
  delay(2000);
  digitalWrite(7,LOW);
  
  // Reverse sequence
  digitalWrite(6,HIGH);
  delay(2000);
  digitalWrite(6,LOW);
  digitalWrite(5,HIGH);
}
