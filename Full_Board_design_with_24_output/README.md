# Relay Control using ESP8266, Ultrasonic Sensors and 74HC595 Shift Registers
This project demonstrates how to control 32 relays using an ESP8266 board, two ultrasonic sensors, and 74HC595 shift registers. The ESP8266 board reads the input from the ultrasonic sensors and uses it to control the state of the relays. If the distance from both sensors is less than 30cm the 32 relays will open in sequence with a delay of 500ms between each relay.


## Hardware Components
•	ESP8266 board (e.g. NodeMCU)
•	Two ultrasonic sensors
•	32 Relays
•	74HC595 shift registers (2 pieces)
•	TIP41C transistor
•	Jumper wires
•	Breadboard
•	Power supply



## Circuit Diagram
### The circuit diagram is composed of :
•	ESP8266 board : which is connected to the ultrasonic sensors and the 74HC595 shift registers
•	Two ultrasonic sensors : are connected to the ESP8266 board
•	32 Relays: are connected to the 74HC595 shift registers
•	74HC595 shift registers: are connected to the ESP8266 board to control the state of the relays
•	TIP41C transistor : is connected to the ESP8266 board to control the state of the relays

## Software

The software for this project is written in C++ using the Arduino IDE. The code is responsible for reading the input from the ultrasonic sensors and using it to control the state of the relays.

## Installation
1.	Download and install the Arduino IDE from the Arduino website.
2.	Connect your ESP8266 board to your computer using a micro-USB cable.
3.	Open the Arduino IDE and go to File > Preferences. In the Additional Boards Manager URLs field, enter http://arduino.esp8266.com/stable/package_esp8266com_index.json.
4.	Go to Tools > Board > Boards Manager. Search for esp8266 and install the latest version.
5.	Select your ESP8266 board from the Tools > Board menu.
6.	Open the code file from this project and upload it to the ESP8266 board by clicking the Upload button.
7.	Make sure the circuit is wired correctly and power it on.
8.	The relays should turn on and off in sequence when the ultrasonic sensors detect an object less than 30cm away.

## Conclusion
This project shows how to use an ESP8266 board, ultrasonic sensors, and 74HC595 shift registers to control multiple relays. It can be used as a starting point for more advanced projects that require control of multiple outputs. The TIP41C transistor and 74HC595 shift registers are used to drive the relays and allow the ESP8266 to control more relays than it could with its own limited output pins. This project is a basic example, and you may need to make some modifications to suit your specific requirements.
Please let me know if there is something else that I can help you with.

