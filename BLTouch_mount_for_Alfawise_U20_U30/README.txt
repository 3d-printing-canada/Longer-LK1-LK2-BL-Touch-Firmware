                   .:                     :,                                          
,:::::::: ::`      :::                   :::                                          
,:::::::: ::`      :::                   :::                                          
.,,:::,,, ::`.:,   ... .. .:,     .:. ..`... ..`   ..   .:,    .. ::  .::,     .:,`   
   ,::    :::::::  ::, :::::::  `:::::::.,:: :::  ::: .::::::  ::::: ::::::  .::::::  
   ,::    :::::::: ::, :::::::: ::::::::.,:: :::  ::: :::,:::, ::::: ::::::, :::::::: 
   ,::    :::  ::: ::, :::  :::`::.  :::.,::  ::,`::`:::   ::: :::  `::,`   :::   ::: 
   ,::    ::.  ::: ::, ::`  :::.::    ::.,::  :::::: ::::::::: ::`   :::::: ::::::::: 
   ,::    ::.  ::: ::, ::`  :::.::    ::.,::  .::::: ::::::::: ::`    ::::::::::::::: 
   ,::    ::.  ::: ::, ::`  ::: ::: `:::.,::   ::::  :::`  ,,, ::`  .::  :::.::.  ,,, 
   ,::    ::.  ::: ::, ::`  ::: ::::::::.,::   ::::   :::::::` ::`   ::::::: :::::::. 
   ,::    ::.  ::: ::, ::`  :::  :::::::`,::    ::.    :::::`  ::`   ::::::   :::::.  
                                ::,  ,::                               ``             
                                ::::::::                                              
                                 ::::::                                               
                                  `,,`


http://www.thingiverse.com/thing:3526108
BLTouch mount for Alfawise U20 U30 by Kana00 is licensed under the Creative Commons - Attribution license.
http://creativecommons.org/licenses/by/3.0/

# Summary

Be careful, this is a modification that requires you to change your 3D printer motherboard.

Attention: You must print this part with 100% infill.

The settings below will help you to configure Marlin:

```cpp
#define X_MIN_ENDSTOP_INVERTING true
#define Y_MIN_ENDSTOP_INVERTING true
#define Z_MIN_ENDSTOP_INVERTING true
#define Z_MIN_PROBE_ENDSTOP_INVERTING false
#define Z_MIN_PROBE_USES_Z_MIN_ENDSTOP_PIN
#define USE_XMIN_PLUG
#define USE_YMIN_PLUG
#define USE_ZMIN_PLUG
#define BLTOUCH
#define X_PROBE_OFFSET_FROM_EXTRUDER -35
#define Y_PROBE_OFFSET_FROM_EXTRUDER -5.5
#define Z_PROBE_OFFSET_FROM_EXTRUDER 0
#define MULTIPLE_PROBING 2
#define X_BED_SIZE 300 // Size for Alfawise U20
#define Y_BED_SIZE 300 // Size for Alfawise U20
#define Z_MAX_POS 400 // Size for Alfawise U20
#define AUTO_BED_LEVELING_BILINEAR
#define GRID_MAX_POINTS_X 5
#define GRID_MAX_POINTS_Y GRID_MAX_POINTS_X
#define Z_SAFE_HOMING
#define EEPROM_SETTINGS
#define NUM_SERVOS 1
#define SERVO_DELAY { 300 }
```

# Print Settings

Printer: Alfawise U20
Rafts: No
Supports: Yes
Resolution: 0.16
Infill: 100%

# Post-Printing

![Alt text](https://cdn.thingiverse.com/assets/07/fc/52/94/da/Example_BLTouch.jpeg)