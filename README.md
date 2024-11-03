# Private_Chat_Via_ESP328266 WebSocket via Lora RA-02 Chat Server with User Authentication


Developed by Vohala, this project is a powerful LoRa-based chat application for the ESP8266 microcontroller. It allows real-time communication over a custom web interface, with user registration, login, and LoRa mesh networking to extend communication over long distances.
Features

Wi-Fi access point creation for user connection.
    User authentication and session management.
    Real-time chat over WebSocket.
    LoRa mesh communication for message relay between nodes.
    EEPROM-based user data storage.

Required Libraries

Make sure to have these libraries installed in your Arduino IDE:

ESP8266WiFi (Built-in)
    ESP8266WebServer (Built-in)
    EEPROM (Built-in)
    WebSocketsServer
    ArduinoJson
    RadioHead
    Hash (Built-in)
    SPI (Built-in)

Pin Configuration

  Connect the ESP8266 to the LoRa RA-02 module as follows:
|LoRa RA-02 Pin	| ESP8266 Pin|
|---------------|------------|
|MISO	| D6 (GPIO12)|
|MOSI	| D7 (GPIO13)|
|SCK	| D5 (GPIO14)|
|NSS (CS)	| D2 (GPIO4)|
|RST	| Not Connected|
|DIO0	| D1 (GPIO5)|
|3.3V	| 3.3V|
|GND	| GND|

Quick Start Guide


Install the ESP8266 board package in your Arduino IDE.

Connect your ESP8266 to the LoRa RA-02 module as per the pin configuration above.

Upload the code to your ESP8266.
Connect to the Wi-Fi network **_"Vohala"_** using the password **_"Vohala_Horizon"_**.
Open a browser and go to http://192.168.4.1 to access the chat application.

Notes

    The LoRa frequency used is 433.0 MHz. Ensure this is suitable for your location.
    Ensure a stable 3.3V power supply to the LoRa module for reliable operation.

Developed by Vohala – Innovating the way we communicate.
