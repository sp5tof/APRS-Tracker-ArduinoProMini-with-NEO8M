# APRS-Tracker-ArduinoProMini-with-NEO8M v1.0
This project is based on Billy's project : https://github.com/billygr/arduino-aprs-tracker & ESP32 iGate project https://github.com/nakhonthai/ESP32APRS_Audio
More informations: https://www.billy.gr/arduino-aprs-tracker/ .

It consists of two independent uC: Arduino Pro-Mini for TNC transmition and ESP-Wroom32 with OLED board for visual decoding incoming APRS frames.
Attached Eagle STL/BRD PCB allows to put them all together.
Baofeng is used as transceiver for this project and connected with two embedded mini-jacks for TX/RX datas & PTT triggering.

I changed few things related to genuine project(Arduino Pro-Mini part):
- support for NEO8M GPS module (TinyGPS library has to be changed, I added the modified library here)
- small change made on original Billy's arduino code related to GPS module
- I used Arduino Pro mini in 5V version and adopted author's code to use this one
- added additional button for changing the APRS symbol(pressing it during the powering ON the device would change the symbol from "car" to "walking man")
  
Cable required for connecting the Baofeng with the device you have to make on your own. I wasn't able to find fully compatible 4-pins (MIC, SPK, PTT, GND) cable with any well-known online stores. However, you can try to order the baofeng audio cable from chinese online store, but the additional changes will have to be made according the the attached schema.

![aprs_prototype](https://github.com/user-attachments/assets/40e736f6-90e2-47d5-a0e7-e9b05a96ee4d)

Kuba/SP5TOF!

