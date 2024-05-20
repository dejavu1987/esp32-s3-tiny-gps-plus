# ESP32 TinyGPSPlus Example
This project demonstrates the use of the TinyGPSPlus library with an ESP32 microcontroller and a GPS module. It receives data from the GPS module and parses it to extract information such as location, date, and time.

## Features
- Uses the TinyGPSPlus library for GPS data parsing.
- Connects to a GPS module via SoftwareSerial.
- Prints GPS information to the serial monitor every 10 seconds.
- Detects and reports if no GPS signal is detected.


![IMG_20240520_154921062~2](https://github.com/dejavu1987/esp32-s3-tiny-gps-plus/assets/1720245/f28fbae7-593f-469a-909e-481f6d8cc1cc)

<img width="590" alt="Screenshot 2024-05-20 at 15 50 33" src="https://github.com/dejavu1987/esp32-s3-tiny-gps-plus/assets/1720245/7d6fc158-7f9e-443e-97d4-fea433663a2e">


## Hardware Requirements
- ESP32 microcontroller (e.g., ESP32-S3-DevKitC-1)
- GPS module with 9600 baud rate (e.g., u-blox NEO-6M)
- Jumper wires

## Software Requirements
- Arduino IDE
- PlatformIO
- TinyGPSPlus library (https://github.com/mikalhart/TinyGPSPlus)
- EspSoftwareSerial library (https://github.com/plerup/EspSoftwareSerial)

## Setup
Connect the GPS module to the ESP32 as follows:
- GPS TX to ESP32 RX (pin 4)
- GPS RX to ESP32 TX (pin 5)
- GPS GND to ESP32 GND
- GPS VCC to ESP32 3.3V

Install the required libraries in the Arduino IDE or PlatformIO.
- Upload the code to the ESP32.
- Open the serial monitor and observe the GPS information being printed every 10 seconds.

## Usage
The code will automatically start receiving and parsing data from the GPS module. The following information will be printed to the serial monitor:

- Location (latitude and longitude)
- Date (month, day, year)
- Time (hour, minute, second, centisecond)
If no GPS signal is detected, the code will print a message indicating that the wiring should be checked.

## Additional Notes
The baud rate of the GPS module can be adjusted in the code if needed.
The interval for printing GPS information can be changed by modifying the interval variable.
This example uses SoftwareSerial for communication with the GPS module. If your ESP32 has dedicated hardware serial ports, you can use those instead.

## Resources
- TinyGPSPlus library: https://github.com/mikalhart/TinyGPSPlus
- EspSoftwareSerial library: https://github.com/plerup/EspSoftwareSerial
- ESP32 documentation: https://docs.espressif.com/projects/esp-idf/en/latest/esp32/

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your changes.
