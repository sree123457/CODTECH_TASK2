Name: SREENIJA KONDURU 
Company: CODTECH IT SOLUTIONS
ID: CT12DS2289 
Domain: Embedded Systems 
Duration: August to October 2024

** Overview of Task2**


DHT sensors (DHT11, DHT22) are commonly used for measuring temperature and humidity. 
These sensors are digital and communicate with a microcontroller (like Arduino) via a single data line. Here is the theoretical background for interfacing a DHT sensor with Arduino.

1. DHT Sensor Overview
DHT11: Measures temperature (0–50°C, ±2°C accuracy) and humidity (20–80%, ±5% accuracy).

2. Pin Configuration
VCC: Power supply (3.3V or 5V)
GND: Ground
DATA: Data pin (connected to a digital pin on Arduino)

3. Single-Wire Communication
DHT sensors use a custom protocol based on the single-wire communication technique, where the microcontroller sends a start signal, and the sensor responds with temperature and humidity data.
Start Signal: The Arduino pulls the data line low for at least 18ms to signal the sensor.
Response Signal: After receiving the start signal, the sensor pulls the data line low for 80µs and then high for 80µs to signal it’s ready.
Data Transmission: The sensor transmits 40 bits of data (8 bits for integral humidity, 8 bits for decimal humidity, 8 bits for integral temperature, 8 bits for decimal temperature, and 8 bits for checksum).
The Arduino reads these bits and processes the data to obtain the temperature and humidity values.

4. Interfacing Steps
Step 1: Connect the DHT sensor to the Arduino.
VCC to 5V (or 3.3V), GND to GND, and DATA pin to a digital pin (e.g., pin 2).
Step 2: Install the DHT sensor library in Arduino IDE to simplify communication.
Step 3: Write Arduino code to initialize the sensor, read data, and print it on the serial monitor.


5. Timing Requirements
Proper timing is essential since the data line must be precisely controlled during communication. The DHT library manages this timing, making communication easier for beginners.

Conclusion:
Interfacing a DHT sensor with an Arduino is straightforward, using the DHT library for communication and a simple wiring setup. The sensor provides digital temperature and humidity data that can be read using the Arduino and displayed on the serial monitor for various applications like weather monitoring and environmental sensing.
