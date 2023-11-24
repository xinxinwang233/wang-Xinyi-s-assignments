# Final Project

## pcb: fernsporeino

***JLC link***

https://u.lceda.cn/join?type=project&key=5c8e20e8195e495293fc84f772aad46e&inviter=7e8bd668f5c34a3faca0e44cb1749f67

***Coding***
```
const int vibrationSensorPin = 4;  //Vibration sensor PIN4
const int magnetPin = 12;          //EMagnet PIN 12
int sensorReading;                 //
int reversesensorReading;

int sumsecond;

long previousTime = 0;
long interval = 4000;  //Set the time of magnet off

void setup() {
  pinMode(vibrationSensorPin, INPUT);
  pinMode(magnetPin, OUTPUT);
  digitalWrite(magnetPin, HIGH);
  Serial.begin(9600);
}

void loop() {

  sensorReading = digitalRead(vibrationSensorPin);  //Read the sensor signal
  unsigned long currentTime = millis();

  bool magnetOn = digitalRead(magnetPin);
  if (sensorReading == 0) {
    previousTime = currentTime;
    digitalWrite(magnetPin, LOW);
  }

  if (currentTime > previousTime + interval) {
    digitalWrite(magnetPin, HIGH);
  }

  Serial.println(sensorReading);
}
```

***POSTER***

<img width="730" alt="截屏2023-11-24 11 12 02" src="https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/74b3a11c-2fe2-4f3c-ad4c-4ec105df50f8">

[poster_fernsporeino_画板 1.pdf](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/files/13454796/poster_fernsporeino_.1.pdf)



***Pictures***

![studio5036](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/d0b32708-3baa-4a97-8b12-c47e8e481bc3)
![studio5035](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/a233d79b-7c98-4090-9948-d47018288179)
![studio5034](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/1d4503b2-5dc3-44be-93fc-d9a11364822f)
![studio5033](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/e1b9309c-33e2-47bc-b5b4-83ea0971456f)
![studio5032](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/e37d0daf-1ca7-4658-b55d-724903b686e1)
![studio5031](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/1914fca3-01ab-47fd-bb11-59b5561893f1)
![studio5030](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/d8c22f92-6fd3-43de-812a-5c5114401333)
![studio5026-1](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/7ed9ca27-c435-4829-ac90-374a91fa7a24)
![IMG_9402](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/d25a73fb-355c-4192-a0a0-2855a250d029)
![IMG_9391](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/d3ef1672-1c3a-4bcb-ba13-870319241c44)

