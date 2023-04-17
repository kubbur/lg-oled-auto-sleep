forked for my convenience

# Auto Sleep LG OLED TV with Motion Sensor
![](images/Prototype_Case.jpg)

I built a device to automatically turn on/off my LG OLED TV screen with a presence sensor. I use this TV as a computer montior, so this helps protect the OLED against burn in when I'm away from the display.

You can see a demonstration of the solution on YouTube: [My Anti Burn-In Prototype for my OLED TV Monitor](https://youtu.be/76wAEJOdBq8)

My implementation includes the following components:
- LilyGo TTGO T-Display ESP32 Controller
- LD2410C Presence Sensor
- Home Assistant Server (to send commands to my LG OLED TV) 

## Wiring
ESP32  |  LD2410C   
5V      <-> VCC  
GND     <-> GND  
GPIO 13 (Configurable)     <-> OUT  

![](images/OLED_Auto_Sleep_Wiring.jpg)


Arduino IDE

in preferences > File
paste in additional board  https://dl.espressif.com/dl/package_esp32_index.json 
in board side panel get esp32 platform

in library manager on the side panel
search for "tft _espi" by Bodmer and install
search for "Button2" by Lennart Hennings

open C:\Users\kubbur\Documents\Arduino\libraries\TFT_eSPI\User_Setup_Select.h

comment //#include <User_Setup.h>  
uncomment #include <User_Setups/Setup25_TTGO_T_Display.h>

