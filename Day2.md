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

Problem of floating- due to middle line, fluctuation

if we press the button then it is connected and output is 1 but if we leave then it fluctuates (connected to nothing) **ir floates**  (like an antenna picking some signal).  it is reliable.

2 solution to this - use INPUT_PULLUP or add resistor (pulldown)

There are two tyoes of input -  INPUT(with resistor), INPUT_PULLUP(without resistor) (please check details in slides)

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


Add 10kohm pull down resistor , it will fix floating problem

we are using 10kohm so that not much current is drained 

Now we can integrate both code (push button and LED code)

const int switchPin = D1;

const int ledPin = D2;

int buttonState = 0;

void setup(){

pinMode(switchPin,INPUT);

pinMode(ledPin,OUTPUT);

Serial.begin(9600);

digitalwrite(ledpin,LOW);   // good practice to keep it this as default

}

void loop(){

buttonState = digitalRead(D1);

Serial.println(nuttonState);

if (bottonState == "0"){

digitalWrite(ledPin,HIGH);

}

else if (buttonState == "1")

{

digitalWrite(ledPin,LOW);

}

else{

Serial.println("erroe");

}
}


// high,low is opposite for builtin LED because it is actively low


## Functions












