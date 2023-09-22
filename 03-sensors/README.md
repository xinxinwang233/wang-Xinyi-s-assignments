# shock sensor 

这是一个震动传感器，它有一个vcc引脚、一个gnd引脚和一个信号引脚，我把信号引脚连接在2号口。此外，我接了一个LED来反映震动传感器有信号或没有。


![IMG_8968.jpg](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/03-sensors/images/IMG_8968.jpg)

当我震动这个震动传感器的时候，传感器上的提示灯会相应亮起，理论上来说，它短暂地发出一个信号。

![IMG_8953.GIF](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/03-sensors/images/IMG_8953.GIF)

这是我编写的程序

`int ledpin=11;                   // Set led pin at Arduino pin 11`  
`int shocksensor=3;               // Set sensor pin at Arduino pin 8`  
`int sensorvalue;                 // initialize variable to store sensor data  
void setup()`  




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

# watersensor


