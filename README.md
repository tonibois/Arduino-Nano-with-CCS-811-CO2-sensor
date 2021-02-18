# Arduino-Nano-with-CCS-811-CO2-sensor

CO2 sensor wired to Arduino Nano that outputs CO2 concentration values in serial monitor and plotter of arduino. Also a buzzer sounds when high level concentrations are detected and an RGB light changes its colour when it is below some concentration.

+ Buzzer sounds when CO2 concentration is bigger than 800
+ RGB LED is red when CO2 > 1000 ppm
+ RGB LED is blue color when (800 < CO2 < 1000) ppm 
+ RGB LED is off when concentration is below 800
+ Optionally uncoment code lines to obtain blue (600 < CO2 < 800) ppm and green (C02 < 600 ppm) 

## Required Material 

1. CCS-811 Sensor
2. Arduino Nano
3. Breadboard
4. Buzzer
5. RGB LED
6. Computer with Arduino IDE installed 
7. Cables
8. Resistances (0.2k, Optional)

# Required Libraries 
Adafruit_CCS811

# Sketch

![alt text](https://github.com/tonibois/Arduino-Nano-with-CCS-811-CO2-sensor/Sketch.png)

# Real circuit



# Acknowledgements
Thanks to mighelangelcasanova for sharing initial code:

https://github.com/miguelangelcasanova/codos/blob/master/dev/arduino/plotter/plotter.ino 
