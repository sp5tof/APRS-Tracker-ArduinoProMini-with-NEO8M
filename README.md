# APRS Tracker/Decoder based on ArduinoProMini, ESP32 & NEO8M GPS receiver module
This project is based on:

- Billy's project : https://github.com/billygr/arduino-aprs-tracker  - more informations: https://www.billy.gr/arduino-aprs-tracker/ &
- ESP32 iGate project https://github.com/nakhonthai/ESP32APRS_Audio

It consists of two independent uC: Arduino Pro-Mini for TNC transmition and ESP-Wroom32 with OLED board for visual decoding incoming APRS frames.

Attached Eagle STL/BRD PCB allows to put them all together.

Baofeng is used as transceiver for this project and connected with two embedded mini-jacks for TX/RX datas & PTT triggering.

I changed few things related to genuine project(Arduino Pro-Mini part):
- support for NEO8M GPS module (TinyGPS library has to be changed, I added the modified library here)
- small change made on original Billy's arduino code related to GPS module
- I used Arduino Pro mini in 5V version and adopted author's code to use this one
- added additional button for changing the APRS symbol(pressing it during the powering ON the device would change the symbol from "car" to "walking man")
  
Cable required for connecting the Baofeng with the device you have to make on your own. I wasn't able to find fully compatible 4-pins (MIC, SPK, PTT, GND) cable with any well-known online stores. However, you can try to order the baofeng audio cable from chinese online store, but the additional changes will have to be made according the the attached schema.

In case of ESP32 part, please follow the manual within the link mentioned above on the nakhonthai github page. 
You have to flash the ESP board. You don't need to configure anything within the ESP32. 
Decoding functionality which is used in this project, works by default without any additional configurations steps to be performed.
I used the ESP-WROOM32 board with embedded OLED display, which works correctly(with version 13a of firmware version, added to this library. However, please use the newest available release on the nakhonthai github page, which should works correctly).

![aprs_prototype](https://github.com/user-attachments/assets/40e736f6-90e2-47d5-a0e7-e9b05a96ee4d)
                                                                                               Kuba/SP5TOF

