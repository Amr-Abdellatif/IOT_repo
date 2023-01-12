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

![TIP41C NPN power transistor](https://user-images.githubusercontent.com/92921252/212137819-77a344cf-2f9d-43d6-9bd6-fb69954eb055.jpg)

![Relay SPDT 5PIN 5V SRD](https://user-images.githubusercontent.com/92921252/212138035-25af53ff-beb2-4291-9f39-6b4a2a682a60.jpg)

![New-Wireless-module-CH340-NodeMcu-V3-Lua-WIFI-Internet-of-Things-development-board-based-ESP8266 jpg_640x640](https://user-images.githubusercontent.com/92921252/212138361-c485f0b8-0182-42f0-a286-a5fb7970d100.jpg)

![41+Wh80XpSL _AC_SY580_](https://user-images.githubusercontent.com/92921252/212138531-3c1142e5-426c-466c-adf9-2f4243848174.jpg)

![71TjtgJG5xL](https://user-images.githubusercontent.com/92921252/212138691-937ce501-e29f-44c2-b386-8113ba701f44.jpg)



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
3.	Open the Arduino IDE and go to File > Preferences. In the Additional Boards Manager URLs field, enter arduino.esp8266.com/stable/package_esp8266com .
4.	Go to Tools > Board > Boards Manager. Search for esp8266 and install the latest version.
5.	Select your ESP8266 board from the Tools > Board menu.
6.	Open the code file from this project and upload it to the ESP8266 board by clicking the Upload button.
7.	Make sure the circuit is wired correctly and power it on.
8.	The relays should turn on and off in sequence when the ultrasonic sensors detect an object less than 30cm away.

## Conclusion
This project shows how to use an ESP8266 board, ultrasonic sensors, and 74HC595 shift registers to control multiple relays. It can be used as a starting point for more advanced projects that require control of multiple outputs. The TIP41C transistor and 74HC595 shift registers are used to drive the relays and allow the ESP8266 to control more relays than it could with its own limited output pins. This project is a basic example, and you may need to make some modifications to suit your specific requirements.
Please let me know if there is something else that I can help you with.

