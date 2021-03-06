## diyHue
[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=J5NHHR47MVTMW)  
This project emulates a Philips Hue Bridge that is able to control ZigBee lights (using Raspbee module or original Hue Bridge or IKEA Tradfri Gateway), Mi-Light bulbs (using MiLight Hub), Neopixel strips (WS2812B and SK6812) and any cheep ESP8266 based bulb from market by replacing firmware with custom one. Is written in python and will run on all small boxes like RaspberryPi. There are provided sketches for Hue Dimmer Switch, Hue Tap Switch and Hue Motion Sensor. Lights are two-way synchronized so any change made from original Philips/Tradfri sensors and switches will be applied also to bridge emulator.

![diyHue ecosystem](https://raw.githubusercontent.com/mariusmotea/diyHue/develop/Images/hue-map.png)


### Requirements:
 - python
 - nmap package for esp8266 lights autodiscover ```sudo apt install nmap```
 - python ws4py package only if zigbee module is used ```sudo pip install ws4py```


## TO DO
 - ~~Working directly with ZigBee lights, switches and sensors with RaspBee module~~
 - ~~control IKEA Trådfri lights from HUE applications~~
 - ~~Create ESP8266 bridge device to add MI Lights to Hue Bridge emulator.~~
 - ~~On/Off control for other home devices using virtual lights~~
 - Alarm (~~email notification~~ + eps8266 horn)
 - ~~Hue Entertainment support~~

## Working HUE futures:
  - Control lights (all functions)
  - Control groups (all functions)
  - Scenes (all functions)
  - Routines
  - Wake up
  - Go to sleep
  - Switches (custom esp8266 switches)
  - Autodiscover lights
  
## Working devices and applications:
  - Amazon Alexa (control only the lights)
  - Logitech Harmony
  - Tradfri Gateway
  - Hue Bridge (original + other emulators)
  - Home Assistant
  - Domoticz
  - Openhab
  - Philips Ambilight TV's 
  - Kodi Hue Ambilight
  - Jeedom
 
 ## Working smartphone applications:
  - Hue (official application)
  - hueManic
  - OnSwitch
  - HueSwitcher
  - LampShade

## Not working:
  - Home & Away future from Hue app (require remote api)
  - Google Home (require remote api)
  - Eneco Toon (very likely it use cloud service detection)
  
## Supported lights:
  - WS2812B and SK6812 smart led strips
  - MiLight
  - Yeelight
  - Pwm RGB-CCT
  - Pwm RGBW
  - Pwm RGB
  - Pwm CCT
  - Pwm Dimming (up to 6 lights for every esp8266)
  - On/Off plugs/lights (up to 6 lights for every esp8266)
  - On/Off 433Mhz devices (multiple devices for every esp8266). Credits Mevel
  
## Stability:
All the lights in my house are controlled by this solution so the stability is very important to me as there is no turn back to classic illumination (all switches were replaces with Ikea Tradfri Remotes and holes covered), however i don't use all the functions to perform full tests on every change. What i use currently is Deconz with all Tradfri devices (lights + sensors), Xiaomi Motion Sensor, native ESP8266 bulbs, ESP8266 + WS2812B strips and Xiaomi YeeLight color bulb.
  
Please submit [here](https://github.com/mariusmotea/diyHue/issues/27) any other device/application that is working with this emulator.
  
Check [Wiki page](https://github.com/mariusmotea/diyHue/wiki) for more details  
  
[![Youtube Demo](https://img.youtube.com/vi/c6MsG3oIehY/0.jpg)](https://www.youtube.com/watch?v=c6MsG3oIehY)

I push updates fast so if you want to notified just add this repo to watch

Contributions are welcomed  

Hue living color light project for 3D printing: https://www.thingiverse.com/thing:2773413

## qtHue
You may want to see also my new project [qtHue](https://github.com/mariusmotea/qtHue) that provide a simple user interface for controlling the lights.
![qtHue](https://github.com/mariusmotea/qtHue/blob/master/Screenshot.png?raw=true)


Credits:
  - 
  - [@avinashraja98](https://github.com/avinashraja98) - Hue Entertainment server
  - Federico Zivolo ([@FezVrasta](https://github.com/FezVrasta)) Internal WebGUI
  - [@J3n50m4t](https://github.com/J3n50m4t) - Yeelight integration
  - Martin Černý ([@mcer12](https://github.com/mcer12)) - Yeelight color bulb
  - probonopd https://github.com/probonopd/ESP8266HueEmulator
  - sidoh https://github.com/sidoh/esp8266_milight_hub
  - StefanBruens https://github.com/StefanBruens/ESP8266_new_pwm
  - Cédric @ticed35 for linkbutton implementation.
