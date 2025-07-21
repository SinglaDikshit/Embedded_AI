Sample code for day-2 using External LED not LED_BUILTIN

void setup(){

pinMode(D2,OUTPUT);

}

Void loop(){

digitalWrite(D2, HIGH);

dalay(1000);

digitalWrite(D2, LOW);

delay(1000);

}

Now, we will see how can we add **serial communication**

String command = "";  //initializinf the variable as empty

void setup(){      // executed once

pinMode(D2,OUTPUT);     // led at D2 pin is our output

Serial.begin(9600);    //Baudrate(bits transmitted per second)-9600

Serial.println("Setup Executed");

}

Void loop(){         //repetition

if (Serial.available()){     // we are checking any data given in serial communication

command = Serial.readStringUntil('\n');

command.trim();  //trim extra useless space

Serial.println(command);

if (command = "on")
{

digitalWrite(D2,HIGH); 

}

else if(command = "off")

{

digitalWrite(D2,LOW); \\ low means ON

}

{

Serial.println("Wring Instruction");

}

}

## Notes

Push Button - it have two metal plates that are not touching, when pressed they are touched for a moment. Circuit - on/off

Problem of floating- due to middle line

There are two tyoes of input -  INPUT, INPUT_PULLUP (please check details in slides)

Code snippet

void setup()

{

pinMode(D1,INPUT);

Serial.begin(9600);

}

void loop()

{

int buttonstate = digitalRead(D1);

Serial.println(buttonstate);

}












