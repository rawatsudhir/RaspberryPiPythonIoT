# Overview

This repository contains a solution to take readings from a touch sensor and send them to cloud (Microsoft Azure) for real-time analytics, using Python on a Raspberry Pi running Raspbian OS.

# Prerequisites

1) Raspberry Pi
2) Touch sensor
3) Azure subscription
4) Azure Blob storage/Power BI online account (you can create a free trial at https://www.powerbi.com)

# Steps

To get this to work, follow the steps below:
 Without giving power to the Raspberry Pi yet, make sure you have connected the touch sensor to the Raspberry Pi as per below. Pin mapping of Raspberry Pi is available here.
  
  GND of
      touch sensor to GND (Pin 6) of Raspberry Pi
  VCC of
      touch sensor to 5V PWR (Pin 2) of Raspberry Pi
  SIG of
      touch sensor to GPIO 2 (Pin 3) of Raspberry Pi
 
Note: GND, VCC and SIG are specified near the touch sensor pins.

Connect the HDMI cable from the Raspberry Pi to the Monitor. Also, connect the wired keyboard and wired mouse to the USB slots in the Raspberry Pi.

Power up the Pi, by connecting it to a power socket. Wait for a minute once this is done. If you are using a Raspberry Pi 2, connect the WiFi module to the USB port of the Pi. You will see the Internet icon in the taskbar (usually at the top right of the screen) - select the appropriate SSID and connect to it. (Alternative way : Click on the link and follow the instructions here to configure WiFi for the
Pi). If you are using a Raspberry Pi 3, there is no need to connect a separate WiFi module.

# Configure Python program to send data to Azure IoT hub 
Fork this repo on your raspberry pi or downlaod the code. This repo contains 3 files

1) [Install Azure IoT sdk for python](https://docs.microsoft.com/en-us/azure/python-how-to-install) 
2) sudhirawtest.py:- Open this program and execute it in Python. Now whenever you touch sensor it will display a message on screen
3) devicemanager.py:- Use this program to register device to IoT hub. Make sure to change connection string before executing the program.
4) d2cMsgSender.py :- Use this program to send device data to iot hub on azure. Make sure to change connection string before executing the program.  
