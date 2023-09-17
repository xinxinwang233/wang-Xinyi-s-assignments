# DIY an arduino using a breadboard

**Foreword**

*This post will show you in great detail how to make an arduino with a few parts and a bread plate, so that you don't need to buy an arduino. At the same time, the post will also contain a basic introduction to the parts, but also will be more in-depth understanding of the board structure.*

## PART 1 Know the components used, their position on the arduino, and their functions

![1.png](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/01-breadboard/images/1.png)

1. **USB socket**
   
   Arduino board can be powered by using the USB cable from your computer. All you need to do is connect the USB cable to the USB connection.
2. **Crystal Oscillator**
   
   The crystal oscillator helps Arduino in dealing with time issues. The number printed on top of the Arduino crystal is 16.000H9H. It tells us that the frequency is 16,000,000 Hertz or 16 MHz.
4. **Voltage Regulator**
   
   The function of the voltage regulator is to control the voltage given to the Arduino board and stabilize the DC voltages used by the processor and other elements.
6. **Electrolytic capacitor**
   
8. **Main microcontroller(ATMega328p)**
   
   Each Arduino board has its own microcontroller. You can assume it as the brain of your board. The main IC (integrated circuit) on the Arduino is slightly different from board to board. The microcontrollers are usually of the ATMEL Company. You must know what IC your board has before loading up a new program from the Arduino IDE. This information is available on the top of the IC. For more details about the IC construction and functions, you can refer to the data sheet.

## PART 2 Attach them to the breadboard step by step
  Attention:
* How to straighten a pin if it's crooked (Don't waste it)
* Check the positive and negative
  
1. **Take out a breadboard**

   We need to know which holes on the breadboard are connected to each other, and if you look at this diagram, the holes represented by the red and blue lines on both sides are connected to each other, and the holes in the middle are connected horizontally

2. **Connecting two paths**

   I used two lines to connect the positive and negative poles on the left and right side of the breadboard.

![b2.jpg](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/01-breadboard/images/b2.jpg)

3. **Transformer and two capacitors (voltage regulator)**
   
   These electronics keeps the voltage entering the circuit steady at 5v. We use two capacitors in the two input ports of the transformer, here we must pay attention to the positive and negative terminals, can not be connected in reverse.
   
![b3.JPEG](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/01-breadboard/images/b3.JPEG)

4. **Connect the Main microcontroller ATMega328p**

   The ATMega328p has a small dot in the upper left corner, plug the first row of pins into position 11 of the breadboard. According to the pin instructions of ATMega328p, connect it with the live wire and ground wire (positive and negative), and the other end should also be connected to the positive and negative terminals of the entire circuit.

![5.png](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/01-breadboard/images/5.png)
![b4.JPEG](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/01-breadboard/images/b4.JPEG)

5. **Crystal Oscillator For The ATMega328p**

   The ATMega328p is coupled with a crystal oscillator, and two small capacitors are connected to the crystal oscillator, and the other end of the small capacitor is connected to the negative electrode of the circuit.

![b5.jpg](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/01-breadboard/images/b5.jpg)

6. **Connect an LED light to the circuit to detect whether the circuit is powered on or not**

   LEDs need a resistor to prevent them from burning out, and I burned out a small LED light while making them. This is my second one.
   
![b6.jpg](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/01-breadboard/images/b6.jpg)

## PART 3 Connection and test with the computer

* *Download ‘silicon labs’ and install:：https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers*
* *Connect the usb to the computer*
  
   In arduino, open the blink file in example.
  
![arduino1.png](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/01-breadboard/images/arduino1.png)
![arduino2.png](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/01-breadboard/images/arduino2.png)

   In the comments, we can see that pin 13 is LED_BUILTIN. So in the next step we will connect an LED to pin 13.


1. **Add an LED on the 13 pins**

![b7.jpg](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/01-breadboard/images/b7.jpg)

2. **Connect the usb socket and ATMega328p**

   There are five wires - between usb socket and ATMega328p, rx connected to tx, tx connected to rx, vcc and gnd connect to the positive and negative terminals of the circuit. The dtr is connected to the first hole of the ATMega328p with a small capacitor together.

![b8.jpg](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/01-breadboard/images/b8.jpg)
![c2.jpg](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/01-breadboard/images/c2.jpg)
![c5.JPEG](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/01-breadboard/images/c5.JPEG)

4. **Connect the computer**

   The first thing was to check if it was smoking, if it was hot, which luckily I didn't have. If not, you need to debug, check whether the positive and negative terminals are reversed or the electronic components are broken.

![c1.jpg](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/01-breadboard/images/c1.jpg)

4. **Go upload test file**

   Upload the test file blink！

![c3.png](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/01-breadboard/images/c3.png)


5. **LED BLINK～ Finished everything.**

![c4.GIF](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/blob/main/01-breadboard/images/c4.GIF)

