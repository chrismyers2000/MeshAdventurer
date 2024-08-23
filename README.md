# MeshAdventurer

Check out my new raspberry pi hat for Linux-native meshtastic here: [MeshAdv Pi Hat](https://github.com/chrismyers2000/MeshAdv-Pi-Hat)
## MeshAdventurer is hardware for Meshtastic with Off-Road use in mind.
Stay connected with your friends while off-roading in places far away from civilization. Simply place your MeshAdventurer on your dash or windsheild and plug it in to any power source from 9-28V (or dedicated 5V input), Or Hide it out of sight while using an external roof-mounted antenna for even more range. The MeshAdventurer is powered by [Meshtastic]( https://meshtastic.org/) Firmware and accompying app for Android and iOS. Send and recieve messages to your friends miles away without using the celluar network. 


Some PCB's may be available here: https://frequencylabs.etsy.com



![PCB 3D V1_3](https://github.com/chrismyers2000/MeshAdventurer/blob/df65f4155d864c4f85d2ea64c8bc7dee39f9705f/Photos/V1.3/3D_PCB_V1.3_Top.png)
![PCB 3D V1_3](https://github.com/chrismyers2000/MeshAdventurer/blob/afec7b6476c34c35250408ffd987cfea9e58bddd/Photos/V1.3/3D_PCB_V1.3_Bottom.png)


## Features:
- 1W transmit power for extended range compared to normal Meshtastic hardware (typically 100mW-160mW).
- Wide range voltage input (9-28V), It can be powered by USB or barrel plug making it extremely versitile. You can even power it using a solar panel! 
- OLED display and rotary encoder with "Canned messages", these are messages pre-programmed by you and can be sent without the need of a smart phone. This is especially useful if your phone dies and you are in an emergency situation.
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
- R2 and R3 form a simple voltage divider to be used as a voltage sensor. It is currently set up as a 1:10 divider meaning 10V = 1V. Make sure to change the multiplier accordingly in the Power settings. Solder together the pads labled "V Sense" if using this circuit. It is connected to GPIO35. This is experimental and has not been fully tested.

## Materials 

- PCB SMD components are all on the bottom side of the board, check the BOM for component list. Top side components listed below.
- Ebyte LoRa module: 868MHz and 915Mhz [E22-900M30S](https://a.aliexpress.com/_mMvsri4) or 433Mhz [E22-400M30S](https://www.aliexpress.us/item/3256801621445884.html)
- MCU: [ESP32-WROOM-32D](https://a.aliexpress.com/_mLVYDGo)
- GPS Module: [ATGM336H](https://www.aliexpress.us/item/3256801517715702.html)
- Temp/Hum Module: [BME280](https://www.aliexpress.us/item/2251832663147484.html)
- OLED Display: [SSD1306](https://www.aliexpress.us/item/3256804169233174.html) Pay attention to the VCC and GND pin sequence when ordering this module, it's common to find them reversed.
- Rotary Encoder: [EC11](https://www.aliexpress.us/item/2261799870168498.html)
- SMA Connector: [SMA-KWE903](https://www.lcsc.com/product-detail/RF-Connectors-Coaxial-Connectors_DreamLNK-SMA-KWE903_C914555.html)
- Button: [KH-6X6X5H-TJ](https://www.lcsc.com/product-detail/Tactile-Switches_Shenzhen-Kinghelm-Elec-KH-6X6X5H-TJ_C2837515.html)
- 


## Disclaimer

The hardware is currently in testing phase but should work fine, it all worked on the breadboard. Future versions may include a Li-ion charging circuit. 
