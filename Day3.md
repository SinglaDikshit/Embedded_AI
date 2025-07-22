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

Serial.begin();

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
















