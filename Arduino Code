#include <ESP32Servo.h>

Servo Base;
Servo Shoulder;
Servo Elbow;
Servo Wrist;
Servo Gripper;

const int BaseSer = 13; 
const int ShoulderSer = 14;
const int ElbowSer = 27;
const int WristSer = 26;
const int GripperSer = 25;

const int BasePot = 36;
const int ShoulderPot = 39;
const int ElbowPot = 34;
const int WristPot = 35;
const int GripperPot = 32;    

void setup() {
  Base.attach(BaseSer);
  Shoulder.attach(ShoulderSer);
  Elbow.attach(ElbowSer);
  Wrist.attach(WristSer);
  Gripper.attach(GripperSer);


}

void loop() {
  int BaseVal = analogRead(BasePot);
  int BasePos = map(BaseVal, 0, 4095, 0, 180);
  Base.write(BasePos);

  int ShoulderVal = analogRead(ShoulderPot);
  int ShoulderPos = map(ShoulderVal, 0, 4095, 0, 180);
  Shoulder.write(ShoulderPos);

  int ElbowVal = analogRead(ElbowPot);
  int ElbowPos = map(ElbowVal, 0, 4095, 0, 180);
  Elbow.write(ElbowPos);

  int WristVal = analogRead(WristPot);
  int WristPos = map(WristVal, 0, 4095, 0, 180);
  Wrist.write(WristPos);

  int GripperVal = analogRead(GripperPot);
  int GripperPos = map(GripperVal, 0, 4095, 0, 180);
  Gripper.write(GripperPos);

  delay(10);
}
