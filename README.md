# Workers Safety Monitoring System

## Project Overview
The Workers Safety Monitoring System is an IoT-based smart safety solution designed to improve worker protection in industrial and hazardous environments. The system continuously monitors environmental conditions such as temperature, humidity, and gas levels to detect unsafe situations. It also includes an emergency panic button for workers to request immediate help.

The project uses an ESP8266 microcontroller to collect sensor data and send alerts through Telegram, while also storing data in ThingSpeak for cloud monitoring and analysis. A GPS module is used to track worker location during emergencies.

---

## Features
- Real-time temperature and humidity monitoring
- Gas leakage detection for worker safety
- Emergency panic button for instant alerts
- GPS location tracking during emergencies
- Telegram notification alerts for unsafe conditions
- ThingSpeak cloud integration for remote monitoring
- LCD display for real-time system status
- Buzzer alert for warning notifications

---

## Technologies Used
### Hardware Components
- ESP8266 (NodeMCU)
- DHT11 Temperature and Humidity Sensor
- Gas Sensor
- GPS Module (NEO-6M)
- I2C LCD Display (16x2)
- Panic Button
- Buzzer

### Software & Libraries
- Arduino IDE
- ESP8266WiFi Library
- WiFiClientSecure Library
- ESP8266HTTPClient Library
- Wire Library
- LiquidCrystal_I2C Library
- TinyGPS Library
- DHT Sensor Library
- SoftwareSerial Library

---

## System Architecture
The system continuously reads environmental and safety data using multiple sensors. Temperature and humidity are monitored using the DHT11 sensor, while gas concentration is detected through a gas sensor. The panic button allows workers to manually trigger emergency alerts.

If unsafe conditions are detected, such as high temperature or gas leakage, the system activates a buzzer and sends an alert message to Telegram. During emergencies, GPS coordinates are included to identify the worker’s location. Sensor data is also uploaded to ThingSpeak for remote monitoring.

---

## Working of the System
1. The system starts and initializes all sensors and modules.
2. WiFi connection is established using ESP8266.
3. Sensor data such as temperature, humidity, and gas levels are collected.
4. Values are displayed on the LCD screen.
5. If temperature or gas exceeds the threshold, an alert is sent through Telegram.
6. If the panic button is pressed, an emergency alert with GPS location is sent.
7. Sensor data is uploaded to ThingSpeak cloud platform.
8. The process repeats continuously for real-time monitoring.

---

## Pin Configuration

| Component | Pin |
|------------|-----|
| DHT11 Sensor | D5 |
| Gas Sensor | A0 |
| Buzzer | D6 |
| Panic Button | D0 |
| GPS RX | D7 |
| GPS TX | D4 |

---

## Alert Conditions
The system generates alerts under the following conditions:

- Temperature greater than 40°C
- Gas sensor value greater than 400
- Panic button pressed by worker

During alerts:
- Buzzer turns ON
- Telegram notification is sent
- GPS location is included for emergencies

---

## Cloud Monitoring
The system uses ThingSpeak cloud platform to store:

- Temperature data
- Humidity data
- Panic button status
- Gas sensor readings
- GPS latitude
- GPS longitude

This helps in monitoring worker safety remotely.

---

## Installation Steps

### Step 1: Install Arduino IDE
Download and install Arduino IDE.

### Step 2: Install Required Libraries
Install the following libraries:
- DHT Sensor Library
- LiquidCrystal_I2C
- TinyGPS
- ESP8266WiFi
- ESP8266HTTPClient

### Step 3: Configure WiFi Credentials
Update WiFi details in the code:

const char* ssid = "YOUR_WIFI_NAME";
const char* pass = "YOUR_PASSWORD";

Step 4: Configure Telegram Bot

Update bot token and chat ID:

String botToken = "YOUR_BOT_TOKEN";
String chatID = "YOUR_CHAT_ID";
Step 5: Configure ThingSpeak API

Add ThingSpeak API key:

String ApiKey = "YOUR_API_KEY";
Step 6: Upload Code
Connect ESP8266 to system
Select board and COM port in Arduino IDE
Upload the code
Expected Output
Sensor readings displayed on LCD
Telegram alerts during emergencies
Buzzer activation during unsafe conditions
GPS-based emergency location tracking
Data uploaded to ThingSpeak cloud



Applications
Industrial worker monitoring
Factory safety systems
Mining worker protection
Hazardous workplace monitoring
Construction site safety

AUTHOR : HEMA DEEPIKA
CONTACT : velagahema@gmail.com
