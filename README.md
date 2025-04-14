#include <Servo.h>

Servo myServo;

void setup() {
  myServo.attach(9);
}

void loop() {
  // 从 0° 缓慢转到 180°
  for (int pos = 0; pos <= 180; pos++) {
    myServo.write(pos);
    delay(15);  // 控制速度（值越大转得越慢）
  }

  delay(1000);  // 停1秒

  // 从 180° 缓慢回到 0°
  for (int pos = 180; pos >= 0; pos--) {
    myServo.write(pos);
    delay(15);
  }

  delay(1000);  // 停1秒
}
