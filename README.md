# DashMaster: LED Sim Racing Telemetry display Powered by SimHub

<img width="1834" height="908" alt="carbon fiber sin hub" src="https://github.com/user-attachments/assets/6a26f3dd-eff0-47d0-85d9-fc88e62aa513" />

DashMaster is a practical Sim racing telemetry dash that displays race information such as your current gear, speed, and lap time using an 8x8 LED Matrix and 7 segment displays.

This project was created to add more realistic and immersive driving components to a racing setup. Having external telemetry displays clears up the monitor view for a more immersive experience. It is designed to be attached on top of a Logitech G29/G920/G923 wheelbase and would be seen through the gap on the steering wheel.

<img width="1788" height="889" alt="copy back race hub good" src="https://github.com/user-attachments/assets/8294bc04-ef17-4ff4-817c-5833c37bf735" />
<img width="1925" height="960" alt="carbon fiber head on" src="https://github.com/user-attachments/assets/cbf02fea-abad-49a6-a922-34c79f40e6f9" />

## Features:

- Customizable 8x8 LED Matrix to display current Gear, Shift lights, and car spotters
- 3 digit 7-segment display for current speed
- 6 digit 7-segment display for current lap time
- Powered by Arduino Pro Micro Microcontroller
- Velcro straps to attach securely to any wheelbase
- Configured with SimHub software

<img width="1410" height="2000" alt="Zine" src="https://github.com/user-attachments/assets/7821f045-9207-49bb-9493-e488362055ba" />

## Case

The case is 3d printed in three parts: The rectangular case housing, the top plate, and the support bracket. 15% infill is reccomended.


<img width="2160" height="1082" alt="race hub parts render" src="https://github.com/user-attachments/assets/84c84662-8554-44d3-bf3b-aa029060f634" />

For the design shown in the photo, paint the inner cavity and surrounding cover of the top plate with glossy black and silver, and paint the front outline with glossy red. The back case and mount can be painted white and black. Optionally, you can add a carbon fiber waterslide decal/sticker on the inner or outer shell.

The LED Matrix and 7 segment displays are screwed in using M3 and M2 screws respectively and mounted on female to female 6mm metal standoffs. The Arduino Pro Micro is friction fit into a special slot near the usb port.


<img width="2160" height="1082" alt="internals race hub render" src="https://github.com/user-attachments/assets/98733628-3fb5-4601-899f-79cbf2b25a13" />

The Racing Dash can be used on a desk on its own or mounted onto a wheelbase such as the Logitech G29. Using adhesive velcro straps, stick the hooked side onto the wheelbase behind the wheel in your desired location, then stick the other side onto the base of the Racing Dash. This allows you to still use the Racing Dash on a table.

## Wiring

Connect the CLK, LOAD, and DATAIN pins to the corresponding pins on the microcontroller for both the LED matrix and the segmented displays. All components are connected to the same ground and VCC pin to avoid voltage drops.

Using SimHub, the CLK and LOAD pins do not need to be placed on the specific clk pins or mosi/miso pins on the Pro Micro. The two 7 segment displays must be cascaded together as shown, and the LED matrix wired separately.


<img width="1613" height="695" alt="Screenshot 2026-06-19 122151" src="https://github.com/user-attachments/assets/791ba122-bd92-46ca-abb2-00d9dcb562d6" />

<img width="644" height="469" alt="image" src="https://github.com/user-attachments/assets/fb2befcf-f5dc-4c00-aaf9-6e0d5888bc72" />

## Firmware

This device uses [SimHub](https://www.simhubdash.com/). SimHub is a comprehensive software compatible with hundreds of popular racing games that relays telemetry and game info to the software, which allows you to set up digital displays, screens, and devices that work universally with any racing game. SimHub automatically creates the sketch to run the firmware on your microcontroller.

First [install Simhub](https://www.simhubdash.com/), then navigate to the "arduino" section
Navigate to "My Hardware", then "Open arduino setup tool". 
Choose Arduino Pro Micro as the board and assign the correct usb port.


<img width="574" height="63" alt="image" src="https://github.com/user-attachments/assets/16b683d0-17cf-449a-9b84-33e3b32965a3" />

Add two MAX7221 7 segment modules and one MAX7221 Led Matrix, and assign the pins as shown above in Wiring. 


<img width="576" height="351" alt="image" src="https://github.com/user-attachments/assets/be761895-d857-4b81-89e2-8640fcd2685a" />

Then click "UPLOAD TO ARDUINO" to upload the firmware.

### Customizing your Racing Dash
Navigate to the "Screens" Tab and find "MainScreen".

You'll want to set the first Led Display to "DataCorePlugin.GameData.NewData.SpeedLocal" (this will be your car's speed)


<img width="1420" height="342" alt="Screenshot 2026-06-18 203007" src="https://github.com/user-attachments/assets/2c760e80-9f49-49f0-8fe5-5dab80059153" />

And set the second LED Display to "GameData.CurrentLapTime"


<img width="1246" height="329" alt="Screenshot 2026-06-18 202847" src="https://github.com/user-attachments/assets/d4b92ac5-404d-42d1-832d-f2cf01cbe5cf" />

Then Navigate to RGB Matrix and enable "Gear". Customize the display to your liking. (note the redline color won't change since the Matrix is one color)


<img width="1326" height="453" alt="image" src="https://github.com/user-attachments/assets/7b5fe1ad-86f8-4c1a-b45f-0ab0506947a1" />

You can experiment with other display features in SimHub to customize your Racing Dash. Add car spotters, lap deltas, warning lights, etc.

## Credits
3d Models Used
[Case Screws](https://www.printables.com/model/259465-iso-chc-m3-screws-3d-models-step-files)
[M3 Nut](https://grabcad.com/library/m3-nut-4)
[Segmented Display Part](https://grabcad.com/library/6-digit-led-display-tube-7-segments-46x14mm-tm1637-1)
[Led Matrix Model](https://github.com/ts91/kicad-LED_DotMatrix)
[Component Screws](https://grabcad.com/library/metric-screws-from-m2-x-2-5-to-m2-x-20-1)
[Arduino Pro Micro](https://github.com/joe-scotto/scottokeebs)
