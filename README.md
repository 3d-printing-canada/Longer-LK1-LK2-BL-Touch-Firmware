# Longer-LK1-LK2-BL-Touch-Firmware
In this guide we'll show you how to install and upload firmware and hardware for your BL touch on the Longer LK1/LK2

### UPDATE 12-08-19
The standard (non BL touch) firmwares have been uploaded. Just like the BL touch versions, find the Project.bin file in the main Marlin folder and put that on your SD card for flashing. 

## Bill Of Materials 
### For Longer LK2 / Alphawise U30 
- Longer LK2 OR Alphawise U30 with V0G Motherboard / Connector (Please see the VOG Motherboard image Above to confirm that you have the correct board)
- BL touch: https://3dprintingcanada.com/products/genuine-antclabs-bltouch-sensor
- EX-1000 Extension Cable (For Longer LK2 only): https://3dprintingcanada.com/products/genuine-antclabs-bltouch-extension-cables
- BL Touch 3D Printed Mount (Uploaded to this repository, but here is the Author): https://www.thingiverse.com/thing:3526108

BUY THE COMPLETE KIT: https://3dprintingcanada.com/products/longer-lk2-alfawise-u30-bl-touch-kit
This kit comes with everything you need for the modification, including a pre-soldered extension cable with integrated resistor

NOTE: Longer LK2 will require a longer wire. I would suggest the XD-1800 cables. The Z endstop connector will need to be modified for this printer with some clippers to fit in the two pin slot on the motherboard. 
https://3dprintingcanada.com/collections/antclabs/products/copy-of-genuine-antclabs-bltouch-extension-cables-sm-xd-1800

## Procedure 

The installation procedure is fairly simple. Note that this guide is for motherboards that are V0G - You know your motherboard is this type if you look at the serial number on the motherboard and it ends in 'V0G'

## Configuring Cura

Cura configuration is the same as the Ender 3 cura config - please refer to our video below for the procedure: 
https://youtu.be/dRgWrepDUBE?t=1316

### Hardware Installation 

1) Print and mount your BL touch, no springs required, using the 3D printed Mount. 
2) Connect your BL touch leads to the correct pins on the motherboard as indicated in the wiring diagram.

NOTE: The extension wires must have a 1K 1/8th watt resistor bridging the positive (red) and signal (orange) wires at the motherboard connector for the BL touch (also shown in the wiring diagram). 3D Printing Canada sells the wire pre-soldered with a resistor (for the LK2 only), or you may try it yourself without soldering by sticking one end of the resistor in the top of the connector for each of the wires, securing it with tape. Soldering it to the wires is the best option. 

### Software Installation

3) Navigate into the folder of the printer you want to flash (LK2 is 220 x 220, LK1 is 300 x 300). In the main folder you will see a 'Project.bin' file. Copy that folder onto your SD card and insert it into the printer. Turn the printer on and watch it upload. 
4) When you see the main info screen for marlin appear, turn the printer off. Insert your SD card into your computer again and delete 'project.bin' (failure to do this will mean the firmware will reflash every time). IMPORTANT: You will notice there is now an EEPROM.dat file. DO NOT delete this - as it serves as the Eeprom for your printer (the memory).
5) Re-insert your SD card

## Configuring the BL Touch
NOTES:
i) To navigate to a previous menu, you have to scroll to the top of your current menu and press the topmost option 
ii) The EEPROM data for the Z probe offset is stored on the SD card. If you start the printer without the SD card in it, that setting will not load properly. Always start your printer with the SD card in it. 


6) Turn on your printer. You will notice you have three controls: two blue navigation arrows and a red select button. 
7) Press the select button and use the arrows to nativage to 'Temperature'.
8) Select 'Preheat PLA' from the list, then 'Preheat PLA' from the next menu. This will preheat the printer.
9) Press the select button and use the arrows to navigate to 'Motion'.
10) Select 'Auto Home'. The printer should home and end up in the center of the bed.
11) In the 'Motion' menu, select Move Axis > Move Z > 10mm. Move the axis down until it is at +000.0 mm. 
12) Navigate to the main menu. Go to Configuration > Probe Z offset
13) Put a piece of paper under the nozzle. Move it back and fourth continuously. Press the blue down button and the gantry will slowly start to move down. You may keep your finger on the button. 
14) Once the nozzle grips the paper enough that it makes a little resistance, but the paper can still move, press the red select button. Scroll down in the 'Configuration' menu until you reach 'Store Settings'. Select that a couple times just to be sure. You're done! 


