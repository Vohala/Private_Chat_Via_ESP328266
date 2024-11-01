# Private_Chat_Via_ESP328266 WebSocket Chat Server with User Authentication


This project is an ESP8266-based web server that provides a simple chat application with user authentication using WebSockets. The server hosts an access point and allows multiple clients to register, login, and communicate in a chat room. It saves user credentials in EEPROM and manages active user sessions for chat communication.
Features

    User registration and login
    Basic authentication via session cookies
    Chat functionality using WebSockets
    User sessions stored in EEPROM
    Support for up to 10 users and 10 client sessions

Requirements

To set up and run this project, you need the following:
Hardware

    ESP8266 module

Software

    Arduino IDE (latest version recommended)
    Board and Libraries (install these in Arduino IDE):
        ESP8266 Board Package
            Go to Tools > Board > Boards Manager in Arduino IDE.
            Search for ESP8266 by ESP8266 Community and install it.
        ArduinoJson by Benoit Blanchon
            Go to Sketch > Include Library > Manage Libraries.
            Search for ArduinoJson and install the latest version.
        WebSockets by Markus Sattler
            Go to Sketch > Include Library > Manage Libraries.
            Search for WebSockets and install the latest version.

Setup Instructions

    Clone or Download the Code
        Clone this repository or download the .zip file, then extract it into your Arduino libraries folder.

    Configure WiFi Credentials
        Open ESP8266_Chat_Server.ino and update the ssid and password variables with your desired WiFi SSID and password.

    cpp

    const char *ssid = "Vohala";
    const char *password = "Vohala_Horizon";

    Upload the Code to ESP8266
        Connect your ESP8266 to your computer.
        Select your ESP8266 board in Tools > Board.
        Set the correct Port under Tools > Port.
        Upload the code by clicking the Upload button in the Arduino IDE.

    Access the Chat Application
        Once the code is uploaded, the ESP8266 will create a WiFi access point with the configured SSID.
        Connect to this WiFi network on your computer or smartphone.
        Open a web browser and navigate to http://192.168.4.1 to access the chat server.

Usage

    Register a New User
        Access the server in a browser.
        Register by filling out the form with a name, email, and password.

    Login
        After registration, login using your credentials.

    Chat
        Once logged in, the chat interface will appear, allowing real-time messaging between connected users.

    Logout
        Click the logout button to end your session.

Code Overview
Key Components

    EEPROM Storage: Stores user credentials in persistent memory.
    ESP8266WebServer: Handles HTTP requests for registration, login, and page rendering.
    WebSocketsServer: Manages chat messages and broadcasts them to connected clients.
    Session Management: Each user session is identified by a unique session ID, managed in cookies.

Functions

    setup(): Initializes WiFi, HTTP server, and WebSocket server.
    handleRegister(), handleLogin(), handleLogout(): Manage user registration, login, and logout.
    displayLoginPage(), displayRegisterPage(), displayChatPage(): Render HTML pages for user interface.
    webSocketEvent(): Handles WebSocket connections, disconnections, and message processing.
