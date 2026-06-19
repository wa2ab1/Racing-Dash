# Sim Racing Telemetry display Powered by SimHub

This Sim Racing Dash is a practical Sim racing addon to your sim racing setup that displays your current Gear, Speed, and Lap Time using an 8x8 LED Matrix and 7 segment displays.

This project was created to add more realistic and cool visual cues to my racing setup. It is designed to be attached on top of a Logitech G29/G920/G923 wheelbase using velcro straps and would be seen through the gap on the steering wheel.

## Features:

- Customizable 8x8 LED Matrix to display current Gear, Shift lights, or Shift warnings
- 3 digit 7-segment display for current speed
- 6 digit 7-segment display for current lap time
- Velcro straps to attach securely to wheelbase
- Powered by Arduino Pro Micro Microcontroller
- Configured with SimHub software

## Case
<img width="2160" height="1082" alt="render racing hub" src="https://github.com/user-attachments/assets/ecc9cbc0-95d9-4233-9567-9439b2a07071" />

## Software

This device uses SimHub. First isntall Simhub, then navigate to the "arduino" section

Since SimHub creates the sketch for you, use the Arduino Setup window to load the firmware.

Navigate to the "Screens" Tab and find "MainScreen".

You'll want to set the first Led Display to "DataCorePlugin.GameData.NewData.SpeedLocal" (this will be your car's speed)

<img width="1420" height="342" alt="Screenshot 2026-06-18 203007" src="https://github.com/user-attachments/assets/2c760e80-9f49-49f0-8fe5-5dab80059153" />


And set the second LED Display to "GameData.CurrentLapTime"

<img width="1246" height="329" alt="Screenshot 2026-06-18 202847" src="https://github.com/user-attachments/assets/d4b92ac5-404d-42d1-832d-f2cf01cbe5cf" />

Then Navigate to RGB Matrix and enable "Gear". Customize the display to your liking. (note the redline color won't change since the Matrix is one color)
<img width="1326" height="453" alt="image" src="https://github.com/user-attachments/assets/7b5fe1ad-86f8-4c1a-b45f-0ab0506947a1" />
