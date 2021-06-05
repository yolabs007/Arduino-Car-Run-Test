# Arduino Car Run Test

![Arduino car](https://circuitbest.com/wp-content/uploads/2020/07/Arduino-Bluetooth-Car-with-L293D.jpg)


#### `Testing of Arduino`

* Test the Arduino Board by using blinking an In-Built LED (Below code) 

```C++
/*
  This Code is written by Rahul Sharma for Yolabs. 
This is the  simplest code possible to blink in build LED  
Turns inbuild LED on and off at diff frequency to chk your arduino IDE, Arduino and cable is working
Note: please check the port in case you have error while uploadig 
 www.yolabs.in - 2020
  
*/

// the setup function runs once when you press reset or power the board

void setup()
{
  pinMode(13,OUTPUT);
  Serial.begin(9600);
}

void loop()
{
    digitalWrite(13, HIGH);
    
    Serial.println("I am High");
    delay(3000); // Wait for 1000 millisecond(s)
    digitalWrite(13, LOW);
    Serial.println("I am Low");
    delay(3000);
 
}


```

* Change the setspeed to limit the speed of the vehicle


```C++

#include <AFMotor.h>


AF_DCMotor motor1(1, MOTOR12_1KHZ);  // Here Motor 1 is connected to M1
AF_DCMotor motor2(4, MOTOR12_1KHZ);  // Here Motor 2 is connected to M2

 

void setup() 
{       
  motor1.setSpeed(255);   //(Speed Varies from (0 to 255))
  motor2.setSpeed(255);   //(Speed Varies from (0 to 255))

}

void loop(){

  // FORWARD
  
  motor1.run(FORWARD);  
  motor2.run(FORWARD); 
  delay(5000);


  //BACKWARD
  motor1.run(BACKWARD);  
  motor2.run(BACKWARD); 
  delay(3000);

}

```
