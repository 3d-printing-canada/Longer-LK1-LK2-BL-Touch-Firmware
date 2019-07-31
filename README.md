# Longer-LK1-LK2-BL-Touch-Firmware
In this guide we'll show you how to install and upload firmware and hardware for your BL touch on the Longer LK1/LK2

## Bill Of Materials 
Required are: 

- BL touch: https://3dprintingcanada.com/products/genuine-antclabs-bltouch-sensor
- EX-1000 Extension Cable: https://3dprintingcanada.com/products/genuine-antclabs-bltouch-extension-cables
- BL Touch 3D Printed Mount (Uploaded to this repository, but here is the Author): https://www.thingiverse.com/thing:3526108

## Procedure 

The installation procedure is fairly simple. Note that this guide is for motherboards that are V0G - You know your motherboard is this type if you look at the serial number on the motherboard and it ends in 'V0G'

### Hardware Installation 

1) Print and mount your BL touch, no springs required, using the 3D printed Mount. 
2) Use the EX-1000 wires to connect your BL touch leads to the correct pins on the motherboard as indicated in the wiring diagram

### Software Installation

3) Navigate into the folder of the printer you want to flash (LK2 is 220 x 220, LK1 is 300 x 300). In the main folder you will see a 'Project.bin' file. Copy that folder onto your SD card and insert it into the printer. Turn the printer on and watch it upload. 
4) When you see the main info screen for marlin appear, turn the printer off. Insert your SD card into your computer again and delete 'project.bin' (failure to do this will mean the firmware will reflash every time). IMPORTANT: You will notice there is now an EEPROM.dat file. DO NOT delete this - as it serves as the Eeprom for your printer (the memory).
5) Re-insert your SD card

##
