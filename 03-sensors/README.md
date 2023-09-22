# shock sensor   
This is a vibration sensor, it has a vcc pin, a gnd pin and a signal pin, I connected the signal pin to port 2. Also, I connected an LED to reflect whether the vibration sensor had a signal or not.  

![IMG_8972.jpg](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/03-sensors/images/IMG_8972.jpg)  

![IMG_8968.jpg](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/03-sensors/images/IMG_8968.jpg)  
When I vibrate this vibration sensor, the light on the sensor lights up accordingly, and in theory, it briefly sends out a signal.  
![IMG_8953.GIF](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/03-sensors/images/IMG_8953.GIF)  
This is the code I wrote.  
```
int ledpin=11;                   // Set led pin at Arduino pin 11  
int shocksensor=3;               // Set sensor pin at Arduino pin 8  
int sensorvalue;                 // initialize variable to store sensor data  
void setup()
{
 pinMode(ledpin,OUTPUT);       // LED pin set to output
 pinMode(shocksensor,INPUT);  //shock sensor pin set to input
 Serial.begin(9600);        // set baud rate for Serial communication
}
void loop() 
{
 sensorvalue = digitalRead(shocksensor); // read values from sensor pin and store in variable
  Serial.println(sensorvalue);
 if (sensorvalue==HIGH)      // if shake detected

 {
  digitalWrite(ledpin,HIGH);   // turn LED on
  Serial.println("vibration detected system awake"); // Print message 
 }
 else{
  digitalWrite(ledpin,LOW);   // turn LED off
  Serial.println("Sleep mode");  // Print message
 }
                 // delay 
}

```  
And I get some feedback  
![IMG_8970.jpg](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/03-sensors/images/IMG_8970.jpg)  


# watersensor


