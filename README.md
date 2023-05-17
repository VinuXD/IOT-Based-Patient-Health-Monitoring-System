# IoT Patient Health Monitoring System

This program enables an IoT-based patient health monitoring system using the MAX30100 pulse oximeter sensor, a LiquidCrystal I2C display, and WiFi connectivity. It measures the patient's heart rate (BPM), blood oxygen level (SpO2), and body temperature. The data is displayed on the LCD and can be accessed through a web server.

## Hardware Requirements

- MAX30100 pulse oximeter sensor
- LiquidCrystal I2C display (compatible with the PCF8574 I/O expander)
- ESP32 or ESP8266 development board
- USB cable for programming and power supply
- Jumper wires
- Breadboard or PCB for circuit connections

## Software Requirements

- Arduino IDE (version 1.8.13 or later)
- MAX30100 PulseOximeter library by Connor Huffine
- LiquidCrystal I2C library by Frank de Brabander
- WebServer library by Ivan Grokhotkov
- WiFi library by Arduino
- Wire library by Arduino

## Installation

1. Install the Arduino IDE from the official Arduino website: https://www.arduino.cc/en/software

2. Open the Arduino IDE and navigate to "Sketch" -> "Include Library" -> "Manage Libraries."

3. In the Library Manager, search for and install the following libraries:
   - "MAX30100 PulseOximeter" by Connor Huffine
   - "LiquidCrystal I2C" by Frank de Brabander
   - "WebServer" by Ivan Grokhotkov

4. Connect the MAX30100 sensor and LiquidCrystal I2C display to your development board.

5. Open the "IoT_Patient_Monitoring_System.ino" file in the Arduino IDE.

6. In the Arduino IDE, go to "Tools" -> "Board" and select the appropriate development board (ESP32 or ESP8266).

7. Go to "Tools" -> "Port" and select the correct serial port for your development board.

8. Modify the program with your WiFi network SSID and password. Replace the values of `ssid` and `password` variables with your network credentials.

9. Click the "Upload" button in the Arduino IDE to compile and upload the program to your development bo

10. Once uploaded, the LCD will display the patient's heart rate (BPM), blood oxygen level (SpO2), and body temperature. You can also access this information through a web browser by entering the IP address shown on the LCD.

## Functions and Callbacks
- `onBeatDetected()`: Callback function executed when a heartbeat is detected.
- `scrollMessage(int row, String message, int delayTime, int totalColumns)`: Scrolls a message on the LCD screen.
- `handle_OnConnect()`: Handles the root URL ("/") request from the web server and sends the health data as an HTML response.
- `handle_NotFound()`: Handles the not found URLs and sends a 404 response.
- `SendHTML(float BPM, float SpO2, float bodytemperature)`: Generates an HTML page with the health data.

## Usage

- The LCD will display the patient's heart rate (BPM), blood oxygen level (SpO2), and body temperature.
- Access the patient's health information by entering the IP address shown on the LCD into a web browser.
- The web page will display the heart rate, blood oxygen level, and body temperature readings.

## Contributing

Contributions to this project are welcome. Feel free to open issues and submit pull requests to improve the program.

## License

This project is licensed under the [MIT License](LICENSE).
