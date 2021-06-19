# SmartMethods
this contains the project I did for smart method training, it is a tinkercad circuit programmed to rotate 6 servo motors from 0 to 90 degrees
https://www.tinkercad.com/things/bjp0F1bafJb-start-simulating/editel?lessonid=EHD2303J3YPUS5Z&projectid=OIYJ88OJ3OPN3EA&collectionid=OIYJ88OJ3OPN3EA&sharecode=-oJGcQ_htWjF3lJ6ayYPY1g57veEdJ_qaeSnc2YGHso

#include <Servo.h>

int outputvalue1 = 0;

int sensorvalue1 = 0;

int sen2 = 0;

int out2 = 0;

int sen3 = 0;

int out3 = 0;

int sen4 = 0;

int out4 = 0;

int sen5 = 0;

int out5 = 0;

int sen6 = 0;

int out6 = 0;

Servo servo_12;

Servo servo_11;

Servo servo_10;

Servo servo_9;

Servo servo_8;

Servo servo_7;

void setup()
{
  pinMode(A0, INPUT);
  servo_12.attach(12, 500, 2500);

  pinMode(A1, INPUT);
  servo_11.attach(11, 500, 2500);

  pinMode(A2, INPUT);
  servo_10.attach(10, 500, 2500);

  pinMode(A3, INPUT);
  servo_9.attach(9, 500, 2500);

  pinMode(A4, INPUT);
  servo_8.attach(8, 500, 2500);

  pinMode(A5, INPUT);
  servo_7.attach(7, 500, 2500);

}

void loop()
{
  sensorvalue1 = analogRead(A0);
  outputvalue1 = map(sensorvalue1, 0, 1023, 0, 90);
  servo_12.write(outputvalue1);
  sen2 = analogRead(A1);
  out2 = map(sen2, 0, 1023, 0, 90);
  servo_11.write(out2);
  sen3 = analogRead(A2);
  out3 = map(sen3, 0, 1023, 0, 90);
  servo_10.write(out3);
  sen4 = analogRead(A3);
  out4 = map(sen4, 0, 1023, 0, 90);
  servo_9.write(out4);
  sen5 = analogRead(A4);
  out5 = map(sen5, 0, 1023, 0, 90);
  servo_8.write(out5);
  sen6 = analogRead(A5);
  out6 = map(sen6, 0, 1023, 0, 90);
  servo_7.write(out6);
  delay(10); 
}
![Screenshot (38)](https://user-images.githubusercontent.com/86006737/122652770-33fd7b00-d149-11eb-9248-2682dfaf7192.png)

