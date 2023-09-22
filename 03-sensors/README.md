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

I attached the sensor to my breadboard and put it in a water glass
```
// Sensor pins
#define sensorPower 7
#define sensorPin A0

// Value for storing water level
int val = 0;

void setup() {
	// Set D7 as an OUTPUT
	pinMode(sensorPower, OUTPUT);
	
	// Set to LOW so no power flows through the sensor
	digitalWrite(sensorPower, LOW);
	
	Serial.begin(9600);
}

void loop() {
	//get the reading from the function below and print it
	int level = readSensor();
	
	Serial.print("Water level: ");
	Serial.println(level);
	
	delay(500);
  }

//This is a function used to get the reading
int readSensor() {
	digitalWrite(sensorPower, HIGH);	// Turn the sensor ON
	delay(10);							// wait 10 milliseconds
	val = analogRead(sensorPin);		// Read the analog value form sensor
	digitalWrite(sensorPower, LOW);		// Turn the sensor OFF
	return val;							// send current reading
}
```  



When placed in a low water level: 
![IMG_8974.jpg](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/03-sensors/images/IMG_8974.jpg)  

![IMG_8974.jpg](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/03-sensors/images/截屏2023-09-21%2012.21.33.png)  

When placed in a high water level: 

![IMG_8973.jpg](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/03-sensors/images/IMG_8973.jpg)  

![IMG_8973.jpg](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/03-sensors/images/截屏2023-09-21%2012.21.45.png)  
