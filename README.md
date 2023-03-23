# MeshAdventurer
## MeshAdventurer is hardware for Meshtastic with Off-Road use in mind.
Stay connected with your riding buddies while off-roading in places far away from civilization. Simply place your MeshAdventurer on your dash or windsheild, Or Hide it out of sight while using an external roof-mounted antenna for even more range. The MeshAdventurer is powered by [Meshtastic]( https://meshtastic.org/) Firmware and accompying app for Android and iOS. Send and recieve messages to your friends miles away without using the celluar network. 





![3D_Vehicle Station V1 pcb_2023-03-19 (1)](https://user-images.githubusercontent.com/42948238/226155903-f0a3d358-b210-4ae8-a519-7b6a86f0ebf4.png)

## Features:
- 1W transmit power for extended range compared to normal Meshtastic hardware (typically 100mW-160mW).
- Wide range voltage input (6V-30V), It can be powered by USB or barrel plug making it extremely versitile. You can even power it using a solar panel! 
- OLED display and rotary encoder with "Canned messages", these are messages pre-programmed by you that can be sent without the need of a connected smart phone. This is especially useful if your phone dies and you are in an emergency situation.
- Optional Temp/Hum/Pressure sensor can send potentially useful data to the rest of your group.
- On-board GPS will keep sending your position even after your phone is disconnected.
- A buzzer to notify you when messages are recieved. 
- 100% compatible with official Meshtastic DIY V1 firmware so you can stay up to date when new versions are released. No custom firmware needed!

## Instructions:

This is currently a DIY project only. You will have to have the PCBs manufactured and assembled or solder the components yourself. 
I used [JLCPCB](https://jlcpcb.com/) as they are fairly cheap and fast. 20 boards cost me just under $12 USD not including shipping. 
Simply upload the gerber .zip file to JLCPCB and follow the instructions. Most of the components were availible from [LCSC](https://www.lcsc.com/) at the time of writing this. Components such as the ESP32 module, E22-900M30S module, buzzer, OLED display, and GPS all were sourced from Amazon and AliExpress.

- Assemble the power circuit first and verify 5V output before soldering the ESP32 and E22 modules.
- Flash the ESP32 using the lastest [Meshtastic Firmware](https://github.com/meshtastic/firmware/releases). Use the firmware-meshtastic-diy-v1-xxxxx.bin file. 

## Disclaimer

The hardware is currently in testing phase but should work fine, it all worked on the breadboard. 
