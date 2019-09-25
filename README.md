# Longer-LK1-LK2-BL-Touch-Firmware
In this guide we'll show you how to install and upload firmware and hardware for your BL touch on the Longer LK1/LK2. The standard (non BL touch) firmwares have also been uploaded. There are a couple variations of these printers, so there are some important points we need to note to do the conversion successfully: 

### NOTE: Firmwares are no longer named "project.bin" as said in some of the YouTube guides - now they are named after the printer type and motherboard type (i.e. LK1V0G_BLtouch_firmware.bin) 

### VOG Vs V08, V07, V06 Motherboards 
The V0G Style motherboard have a handy little connector you can use to plug the BL touch into - not so on the V08 and previous boards. To determine the style of motherboard in your machine, compare it to the images in this github identifying each board. You will have to use the proper firmware for each board, so make sure that you select the correct firmware for both your board type and printer type.  


# Bill Of Materials 
### For Longer LK2 / Alphawise U30 
- Longer LK2 OR Alphawise U30 with V0G Motherboard / Connector (Please see the VOG Motherboard image Above to confirm that you have the correct board)
- BL touch: https://3dprintingcanada.com/products/genuine-antclabs-bltouch-sensor
- EX-1000 Extension Cable (For Longer LK2 only): https://3dprintingcanada.com/products/genuine-antclabs-bltouch-extension-cables
- BL Touch 3D Printed Mount (Uploaded to this repository, but here is the Author): https://www.thingiverse.com/thing:3526108

BUY THE COMPLETE KIT: https://3dprintingcanada.com/products/longer-lk2-alfawise-u30-bl-touch-kit
This kit comes with everything you need for the modification, including a pre-soldered extension cable with integrated resistor

### For Longer LK1 / Alphawise U20 

- BL touch: https://3dprintingcanada.com/products/genuine-antclabs-bltouch-sensor
- SM-XD-1800 Cables https://3dprintingcanada.com/collections/antclabs/products/copy-of-genuine-antclabs-bltouch-extension-cables-sm-xd-1800

# Hardware Installation 

### Requirements for the V0G board
The extension wires must have a 1K 1/8th watt resistor bridging the positive (red) and signal (orange) wires at the motherboard connector for the BL touch (also shown in the wiring diagram). 3D Printing Canada sells the wire pre-soldered with a resistor (for the LK2 only), or you may try it yourself without soldering by sticking one end of the resistor in the top of the connector for each of the wires, securing it with tape. Soldering it to the wires is the best option. I do this by cutting the  red and orange wires about 10cm from the connector at the same place, stripping the ends, and then soldering both red ends and both orange ends to either end of the resistor. Heat shrink to protect the connections. 

### Requirements for the V08, V07 and V06 boards
The following modifications must be made for the VO8, V07 and V06 boards: 

1) Using your clippers you must clip off the unused 3rd pin of the 3 pin JST-XH (white) connector for the Z probe min signal (if using the 1800mm cables). That will allow you to insert the connector into the right slot when interfacing the BL touch on the motherboar.
2) Remove the red (+5V) wire from the black 3 pin JST connector, put the brown and orange ones together, and then clip off the unused 3rd pin on the black JST connector to make a 2 pin (or use one of the blank 2 pin connectors that come with the BL touch). 
3) Remove / desolder capacitor C29 on the motherboard as marked in the wiring diagram - this can be done with a soldering iron or very carefully by twisting it off with needle nose pliers. 
4) Solder the red +5V wire of the BL touch to the D7 capacitor as shown on the wiring diagram. 

### Hardware Installation Procedure 
1) Print and mount your BL touch, no springs required, using the 3D printed Mount. 
2) Connect your BL touch leads to the correct pins on the motherboard as indicated in the wiring diagram. 
3) Carefully route the BL touch wires through the existing cable management system for the hotend wires.

### Software Installation (For Standard & BL Touch Firmwares)
3) Navigate into the folder of the printer you want to flash (LK2 is 220 x 220, LK1 is 300 x 300). In the main folder you will see a '####_firmware.bin' file. Copy that folder onto your SD card and insert it into the printer. Turn the printer on and watch it upload. 
4) When you see the main info screen for marlin appear, turn the printer off. Insert your SD card into your computer again and delete '####_firmware.bin' (failure to do this will mean the firmware will reflash every time). IMPORTANT: You will notice there is now an EEPROM.dat file. DO NOT delete this - as it serves as the Eeprom for your printer (the memory).
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

## Configuring Cura

Cura configuration is the same as the Ender 3 cura config - please refer to our video below for the procedure: 
https://youtu.be/dRgWrepDUBE?t=1316

Please note: The Ender 3 configuration will work for the LK2, but for the LK1 you should select the "CR-10" default profile and add a G29 to it as per the instructions in the Ender 3 cura config video above. 
