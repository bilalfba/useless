# Useless Box Code
The Code for the useless box

```python

#include <Servo.h>

Servo hand;
int swch = 2;
int pos = 0;

// put your setup code here, to run once:
void setup() {
  
  pinMode(swch, INPUT);
  hand.attach(9);
  hand.write(0);
  //delay(1000);
  Serial.begin(9600);

}

void loop() {

   if(digitalRead(swch) == LOW)
   {
      Serial.println("switch is high");
      hand.write(150);
   }
  
   else 
   {
      Serial.println("switch is low");
      hand.write(0);
   }
   
    delay(500);
}


```
