# Relay Control using ESP8266, Ultrasonic Sensors and 74HC595 Shift Registers
This project demonstrates how to control 32 relays using an ESP8266 board, two ultrasonic sensors, and 74HC595 shift registers. The ESP8266 board reads the input from the ultrasonic sensors and uses it to control the state of the relays. If the distance from both sensors is less than 30cm the 32 relays will open in sequence with a delay of 500ms between each relay.

Hardware Components
ESP8266 board (e.g. NodeMCU)
Two ultrasonic sensors
32 Relays
74HC595 shift registers (2 pieces)
TIP41C transistor
Jumper wires
Breadboard
Power supply
Circuit Diagram
