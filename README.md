# 5" Multi-Channel Smart Somfy Blind Controller with Weather , forcast & Screensaver

## Overview

I developed a custom multi-channel Somfy remote using a low cost 433 MHz transmitter, 
and 5" touchscreen display with internal ESP32 microcontroller. Unlike traditional Somfy remotes with 
limited channels, this DIY solution offers unlimited channel support and advanced 
features like weather forecasting and photo display capabilities.


<br>

<p align="center">
  
![Remote](https://github.com/user-attachments/assets/8409b49d-5db0-4d69-be54-ae2eae4ae10f)

 
</p>

<br>

### Key Features

- Multi-channel remote control with Somfy rolling-code protocol implementation
- Custom-modified RF transmitter optimized for Somfy compatibility
- Intuitive 5-inch HMI touch display interface
- Real-time weather updates via API integration
- Photo slideshow screensaver functionality

## Technical Challenges & Solutions

### RF Transmitter Modification
The first challenge involved modifying the 433.92MHz RF transmitter for Somfy compatibility:
- Required frequency adjustment to 433.42MHz
- Successfully replaced SAW filter through precision soldering
- Verified transmission frequency using RDS testing

![modifiedTx](https://github.com/user-attachments/assets/0e451065-9155-451d-8ad5-c71580fcf5c1)


### ESP32 code Integration
Initially encountered issues with the RemoteSomfy Arduino library on the Elecrow HMI display:
- Identified interrupt conflicts between UI display function and RF transmission
- Implemented FreeRTOS task management solution
- Successfully isolated RF transmission code to Core0 using xTaskCreatePinnedToCore

## Hardware Components

- **Display**: Elecrow 5" HMI touchscreen
- **Transmitter**: Modified 433.9MHz RF module
- **Optional**: External antenna for extended range, External battery supply

  ![TouchScreenBackSide](https://github.com/user-attachments/assets/93fad01e-eee4-4c7b-b129-be598b57eb81)


## Variety of functions and features

- **Unlimited Channels**: Create and manage multiple Somfy blind channels through the touchscreen interface
- **Individual Control**: up/down/stop control for each blind 
- **Group Control**: Operate multiple blinds simultaneously
- **Weather Integration**: Real-time weather data display with forecast information using openweathermap API
- **Screensaver Mode**: Display family photos when idle
- **Custom Interface**: Intuitive touchscreen controls 
- **Rolling Code Security**: Full implementation of Somfy's secure rolling code protocol
- **Extended Range**: Optional antenna support for increased transmission distance

## Result

<p align="center">

https://github.com/user-attachments/assets/4909be1d-0977-4549-ab8b-ba6ec3b59434

</p>
