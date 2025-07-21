## Day1

Sensor Used- XIAO ESP32S3 Sense

The output of every sensor is Voltage, which can be later converted into the desired parameter.

ADD pin diagram ##

We don't need all the sensors each time, we can use software like TinkerCAD to make and test a circuit.

Be careful about the allowed power supply of the sensor.

Data signal types- Digital, Analog, Pulse(Count, Interrupt)

Tx, Rx- UART protocol

Sclk, MISO, MOSI, CS- SPI

Clk, Data- I2C 

Use python 3.10.x
Use Node.js 18.20.x
Use npm 10.x.x

if we dont the keep the python version uniform then we may witness errors

used this command to add edge impulse CLI - npm install -g edge-impulse-cli

default code in Arduino 

`void setup(){`

`.......`

`}`

`void loop(){`

`......`

`}`

Sample project - Blinking LED

void setup(){

pinMode(LED_BUITIN,OUTPUT);

}

Void loop(){

digitalWrite(LED_BUITIN, HIGH);

dalay(1000);

digitalWrite(LED_BUILTIN, LOW);

delay(1000);

}












