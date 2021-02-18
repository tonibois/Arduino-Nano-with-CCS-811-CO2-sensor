# Arduino-Nano-with-CCS-811-CO2-sensor

CO^2 sensor wired to Arduino Nano that outputs CO2 concentration values in serial monitor and plotter of arduino. Also a buzzer sounds when high level concentrations are detected and an RGB light changes its colour when it is below some concentration.

+ CO2 sensor (CCS811)
+ Buzzer sounds when CO2 concentration is bigger than 800 
+ RGB LED is red when CO2 > 1000 ppm
+ RGB LED is blue color when (800 < CO2 < 1000) ppm 
+ RGB LED is off when concentration is below 800
+ Optionally uncoment code lines to obtain blue (600 < CO2 < 800) ppm and green (CO2 < 600 ppm) 



## Required Material 

<center>
1.CO2 sensor (CCS-811)
<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQpCsr3m4kD-yAsh7RNSmo15HEv6KgYtPxiOA&usqp=CAU" width="300" height="300" />

2. Arduino Nano
<img src="https://www.electan.com/images/nano.jpg" width="300" height="300" />

3. Breadboard
<img src="https://cdn.sparkfun.com//assets/parts/8/5/0/3/12002-Breadboard_-_Self-Adhesive__White_-01.jpg" width="300" height="300" />

4. Buzzer
<img src="https://www.pcboard.ca/image/cache/catalog/products/buzzers/piezo-buzzer/piezo-buzzer-01-500x500.jpg" width="300" height="300" />

5. RGB LED
<img src="https://cdn.sparkfun.com//assets/parts/6/5/5/7/11120-Diffused_LED_-_RGB_10mm-01.jpg" width="300" height="300" />


6. Computer with Arduino IDE installed 
7. Cables
8. Resistances (0.2k, Optional)

# Required Libraries 
Adafruit_CCS811

# Sketch

![alt text](https://github.com/tonibois/Arduino-Nano-with-CCS-811-CO2-sensor/blob/main/Sketch.png)

# Real circuit
<center>
![alt text](https://github.com/tonibois/Arduino-Nano-with-CCS-811-CO2-sensor/blob/main/IMG_20210218_011855_703.jpg)
![alt text](https://github.com/tonibois/Arduino-Nano-with-CCS-811-CO2-sensor/blob/main/IMG_20210218_011902_909.jpg){ width=20% }
![alt text](https://github.com/tonibois/Arduino-Nano-with-CCS-811-CO2-sensor/blob/main/IMG_20210218_011914_482.jpg){ width=20% }
![alt text](https://github.com/tonibois/Arduino-Nano-with-CCS-811-CO2-sensor/blob/main/IMG_20210218_011920_044.jpg){ width=20% }
<\center>

# Acknowledgements
Thanks to mighelangelcasanova for sharing initial code:

https://github.com/miguelangelcasanova/codos/blob/master/dev/arduino/plotter/plotter.ino 
