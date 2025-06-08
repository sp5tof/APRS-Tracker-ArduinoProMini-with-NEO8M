# APRS-Tracker-ArduinoProMini-with-NEO8M v1.0
This project is based on Billy's project : https://github.com/billygr/arduino-aprs-tracker .
More informations: https://www.billy.gr/arduino-aprs-tracker/

I changed two things related to genuine project:
- support for NEO8M GPS module (TinyGPS library has to be changed, I added the modified library here)
- small change made on original Billy's arduino code related to GPS module
  
This project will be developed. 
I would like to add AFSK packet analyzer and oled display.
However, LibAPRS library supports only AVR family uC. ESP32 doesn't support atomic commands being used by this library. 
That's why Arduino Pro Mini is a must with this project (ESP32 is probably possible but requires additional DAC module).
Kuba/SP5TOF
