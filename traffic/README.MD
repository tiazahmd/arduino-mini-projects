### Automated Traffic Light

**Project Description**: An automated traffic light system controlled by C. Materials used:
- 3 LEDs
- 3 220-ohm Resistors
- 3 Jumper Wires

**Steps**:
1. Place the 3 LEDs side by side (I kept a gap of two pins between the LEDs).
2. Connect the anode (long leg) of the LEDs to pin 5 (Yellow), 6 (Red) and 7 (Green).
3. Connect the cathode (short leg) of the LEDs to the ground through a 220-ohm resistor.
4. Upload the code and the traffic lights should work automatically.

**Code**:
```
void setup() {
    // Setup the pins as outputs:
    pinMode(5, OUTPUT);
    pinMode(6, OUTPUT);
    pinMode(7, OUTPUT);
}

// 5 = Yellow; 6 = Red; 7 = Green;

void loop() {
    // Red light
    digitalWrite(5, LOW);
    digitalWrite(6, HIGH);
    digitalWrite(7, LOW);
    delay(2400);        // Red light will stay on for 2.4 seconds 
                        // before switching to green

    // Green Light
    digitalWrite(5, LOW);
    digitalWrite(6, LOW);
    digitalWrite(7, HIGH);
    delay(3200);        // Green light will stay on for 3.2 seconds
                        // before switching to yellow

    // Yellow Light
    digitalWrite(5, HIGH);
    digitalWrite(6, LOW);
    digitalWrite(7, LOW);
    delay(1800);        // Yellow light will stay on for 1.8 seconds
                        // before switching to red
}
```
**Watch how it works**: ![Watch the video on YouTube](https://youtu.be/NiPdsiJ9Vgo)