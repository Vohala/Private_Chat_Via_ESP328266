# Private_Chat_Via_ESP328266 WebSocket Chat Server with User Authentication


This project creates a simple chat application using an ESP8266 microcontroller, allowing multiple users to register, log in, and communicate over a WiFi network using WebSockets.
Features

    User Registration and Login with session management
    Real-time chat using WebSockets
    User data persistence via EEPROM

Requirements
Hardware

    ESP8266 module

Software

    Arduino IDE
    Libraries (install in Arduino IDE):
        ESP8266 Board Package
            Go to Tools > Board > Boards Manager and search for ESP8266 by ESP8266 Community
        ArduinoJson by Benoit Blanchon
            Go to Sketch > Include Library > Manage Libraries, then search for ArduinoJson
        WebSockets by Markus Sattler
            Go to Sketch > Include Library > Manage Libraries and search for WebSockets

Setup

    Clone/Download Code: Clone this repository or download it as a .zip and extract it.
    WiFi Credentials: Update ssid and password in the code to your preferred WiFi network name and password.
    Upload Code: Connect your ESP8266 to your computer, select the correct board and port, then upload the code using Arduino IDE.

Accessing the Chat Application

    Connect to the ESP8266’s WiFi network.
    Open a browser and go to http://192.168.4.1.
    Register a new user, log in, and start chatting!
