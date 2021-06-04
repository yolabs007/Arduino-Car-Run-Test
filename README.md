# Arduino Car Run Test

* Connect the Arduino to Arduino Shield
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
