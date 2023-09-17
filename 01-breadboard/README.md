# DIY an arduino using a breadboard

**Foreword**

This post will show you in great detail how to make an arduino with a few parts and a bread plate, so that you don't need to buy an arduino. At the same time, the post will also contain a basic introduction to the parts, but also will be more in-depth understanding of the board structure.

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
* 戳到什么程度刚好
* 针脚歪掉怎么捋直（不要浪费）
* 任何元件正负极的检查
  
1. 准备一个面包板
2. 连接两侧通路
3. 变压器和两个电容（稳压器）
4. atmel板和它的火线地线和reset
5. atmel板加上计时器，和两个小电容
6. 并连一个小灯和它的电阻，来检查整个电路的有效性

## PART 3 与电脑的链接和测试
* 下载软件silicon labs
* 链接电脑与上传
1. 增加一个灯在13引脚，并编写相应程序
2. 连线给usb头和面包版
3. 连接电脑，检查是否冒烟，是否发烫
4. 上传文件并显示成功
5. 上传失败的debug方法
6. 成功的小灯闪烁


**bold text**

*italic text*

***italic and bold text***

example of an external link

[description of the website](https://www.https://www.example.com/)

example of a picture hosted on an external website

![picture description](https://djmag.com/sites/default/files/storyimages/Clara_Rockmore.jpg)

example of a picture hosted inside your repository (don't forget the ./ operand)

![picture description](./images/example.jpg)
