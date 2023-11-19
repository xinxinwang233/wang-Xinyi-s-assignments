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

***Pictures***







