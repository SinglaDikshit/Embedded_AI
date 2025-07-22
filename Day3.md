# Sensor Acquisition and Actuator Control

## DHT11 (Digital) sensor

Use "DHT sensor library" by Adafruit (Install dependencies too)

Measure Temperature(0-50 deg C) and Humidity(20%-90%)

Pins- Vcc, GND, Data pin

Code Used-

#include <DHT.h>

#include <Adafruit_Sensor.h>

#DEFINE DHTPIN D2

#DEFINE DHTTYPE DHT11

DHT dht(DHTPIN,DHTTYPE);

void setup(){

Serial.begin(9600);

dht.begin();

}

void loop(){

float temp = dht.readTemperature():

float hum = dht.readHumidity();

if (isnan(temp) || isnan(hum))     \\ trying to know any of the values are not available

{

Serial.println("Failed to read");

}

else {

Serial.println("Temperature:", temp, "deg C");

Serial.println("Humidity: ", hum, "%");

}

}

## Servo motor

Servo motor is an actuator that rotates to specific angles between 0 to 180 (internal feedback maintains that position). This also have 3 pins similarly.

Use ESP32servo Library

Code- 

(First run the codes to detect 0 and 180 position)

#include <ESP32Servo.h>

#define SERVOPin D3

Servo myServo;

void setup(){

myServo.attach(SERVOPin);

myServo.write(0);

}

void loop(){

for (int angle =0; angle <=180;angle+=1)

{

myServo.write(angle);

delay(100);

}

for (int angle =180; angle >=0;angle-=1)

{

myServo.write(angle);

delay(100);

}

}


## Final code 

#include <DHT.h>

#include <ESP32Servo.h>

#include <Adafruit_Sensor.h>

#DEFINE DHTPIN D2

#DEFINE DHTTYPE DHT11

#define SERVOPin D3

DHT dht(DHTPIN,DHTTYPE);

Servo myServo;

void setup(){

Serial.begin(9600);

dht.begin();

myServo.attach(SERVOPin);

myServo.write(0);

}

void loop(){

float temp = dht.readTemperature():

float hum = dht.readHumidity();

if (isnan(temp) || isnan(hum))     \\ trying to know any of the values are not available

{

Serial.println("Failed to read");

}

else {

Serial.println("Temperature:", temp, "deg C");

Serial.println("Humidity: ", hum, "%");

}

delay(2000);

int angle = (temp/50)*180;

myServo.write(angle);

int angl = (hum/100)*180;

myServo.write(angl);

}

\\ we can do one at a time

\*

code used by instructor

// map temp 0-40 deg to 0-180 degree

int angle = map((int)temp, 20, 40, 0, 180);

angle = constrain(angle,0,180);

















