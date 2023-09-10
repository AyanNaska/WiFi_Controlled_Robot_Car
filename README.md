# WiFi_Controlled_Robot_Car

## Overview

This project demonstrates how to build a WiFi-controlled robot car using the ESP32 (Wemos D1 R32) microcontroller, the L298N motor driver, and the Blynk IoT platform. The robot car can be controlled remotely via a mobile app through a WiFi connection. This README provides step-by-step instructions for setting up and using the robot car.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Hardware Components](#hardware-components)
- [Wiring Diagram](#wiring-diagram)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

Before you begin, make sure you have the following prerequisites in place:

- Arduino IDE installed on your computer.
- The ESP32 board support installed in your Arduino IDE.
- The Blynk app installed on your mobile device (Android or iOS).
- Basic knowledge of Arduino programming.

## Hardware Components

To build this robot car, you will need the following hardware components:

- ESP32 (Wemos D1 R32) microcontroller
- L298N Motor Driver
- DC Motors (2x)
- Wheels (2x)
- Chassis or frame for the robot car
- Battery pack or power source
- Jumper wires
- Breadboard (optional)
![IMG_20230910_140833_384](https://github.com/AyanNaska/WiFi_Controlled_Robot_Car/assets/113054786/0f867bdf-7172-49a2-acc0-ffbe62891cf1)
## Wiring Diagram

![ESP32_2Motors_L298_tot_res](https://github.com/AyanNaska/WiFi_Controlled_Robot_Car/assets/113054786/6918d2c7-f9cd-4bc4-ab8c-68b25f363369)


Make sure to connect the components according to the provided wiring diagram. Double-check your connections to avoid any issues.

## Installation

1. Clone or download this GitHub repository to your local machine.
2. Open the Arduino IDE and navigate to `File > Open`. Select the Arduino sketch file (`robot_car.ino`) from the downloaded repository.
3. Configure the Arduino IDE to use the ESP32 board. Select the appropriate board from the `Tools > Board` menu.
4. Connect your ESP32 board to your computer via USB.
5. Upload the sketch to your ESP32 board by clicking the "Upload" button in the Arduino IDE.

## Configuration

Before you can control the robot car with Blynk, you need to configure the Blynk app and the ESP32 code.

### Blynk App Configuration

1. Open the Blynk app on your mobile device.
2. Create a new Blynk project.
3. In the Blynk app, add a joystick widget to control the movement of the robot car.
4. Generate an authentication token for your project in the Blynk app, and note it down.

### ESP32 Code Configuration

1. Open the `robot_car.ino` file in the Arduino IDE.
2. Replace the placeholders in the code with your WiFi network credentials and the Blynk authentication token.

```cpp
const char* ssid = "Your_WiFi_SSID";
const char* password = "Your_WiFi_Password";
char auth[] = "Your_Blynk_Auth_Token";
