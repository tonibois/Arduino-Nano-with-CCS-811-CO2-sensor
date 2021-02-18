// Import libraries
#include "Adafruit_CCS811.h"          // Incluir la librería del sensor
Adafruit_CCS811 ccs;                  // Crear un objeto sensor

// set digital pins in Arduino Nano for RGB LED and Buzzer
int buzzer = 7;
int redLed= 4;
int greenLed = 5;
int BlueLed = 6;


// Set threshold values
int sensorThres1 = 400; 
int sensorThres2 = 600; 
int sensorThres3 = 800;
int sensorThres4 = 1000; 

// Set pin modes (IN/OUT) and begin to search sensors

void setup() {
  pinMode(buzzer, OUTPUT);
  pinMode(redLed, OUTPUT);
  pinMode(greenLed, OUTPUT);
  pinMode(BlueLed, OUTPUT);    
  Serial.begin(115200);               // Initialize serial port
  //  Serial.println("Print CCS811 data");
  Serial.println("CO2, TVOC");
  
  if(!ccs.begin()){                   // Initialize sensor
    Serial.println("Check wiring");
    while(1);
  }
  while(!ccs.available());            
}

void loop() {
  if(ccs.available()){              
    if(!ccs.readData()){             
      int analogSensor=ccs.geteCO2();

    if (analogSensor > sensorThres4)
    {
      digitalWrite(redLed, HIGH);
      digitalWrite(greenLed, LOW);
      digitalWrite(BlueLed, LOW);      
      tone(buzzer, 2000, 500);
      //tone(buzzer, 500, 200);
      //tone(buzzer, 200, 200);
    }
    else if ((analogSensor < sensorThres4) && (analogSensor > sensorThres3))
    {
      digitalWrite(redLed, LOW);
      digitalWrite(greenLed, HIGH);
      digitalWrite(BlueLed, HIGH);   
      tone(buzzer, 500, 200);      
    }
    else if ((analogSensor < sensorThres3) && (analogSensor > sensorThres2))
    {
      digitalWrite(redLed, LOW);
      digitalWrite(greenLed, LOW); //HIGH);
      digitalWrite(BlueLed, LOW);   
      noTone(buzzer);
    }
        else if ((analogSensor < sensorThres2) && (analogSensor > sensorThres1))
    {
      digitalWrite(redLed, LOW);
      digitalWrite(greenLed, LOW);
      digitalWrite(BlueLed, LOW); //HIGH);   
      noTone(buzzer);
    }
    else
    {
      digitalWrite(redLed, LOW); //HIGH);
      digitalWrite(greenLed, LOW); //HIGH);
      digitalWrite(BlueLed, LOW); // HIGH);   
      noTone(buzzer);
    }

      
      Serial.print(ccs.geteCO2());    // Get and print and plot CO2 signal 
      Serial.print(", ");              // split values with comma
      Serial.println(ccs.getTVOC());  // Get and print TVOC
    }
    else{
      Serial.println("ERROR!");       // Check for errors
      while(1);                       
    }
  }
  delay(100);                         // Make measurements each 0.1 s
}
