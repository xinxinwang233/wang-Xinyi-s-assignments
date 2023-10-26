# 电路板雕刻

这一节课我们学习使用SRM-20机器和自己绘制的图片进行电路板的雕刻。下面我将记录全部的操作过程，最终我获得了一块可以使用的DIY电路板。
首先我们使用嘉立创的平台绘制我们的pcb图纸。  
*https://lceda.cn/*  
<img width="1621" alt="截屏2023-10-26 12 56 00" src="https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/e45c5f89-7fcc-437d-9820-831ff4256d60">  
我们需要知道自己使用的原件是什么封装规格，我们所有的封装规格都选择1206。  
<img width="868" alt="截屏2023-10-26 13 03 11" src="https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/1ccf2b67-5322-4b98-bf4e-e7121ae68064">  
选择好所有的原件之后，我们只需要用电线将它们连接起来，这里有一些注意事项。  
<img width="270" alt="截屏2023-10-26 13 04 20" src="https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/3f3571af-b76e-4701-b3d5-4ace43957819">  

连线注意事项
* 需要知道切割机器的刀头大小，并在图纸中主义，不应该有小于刀头的形状。这台机器使用两个倒，0.4mm和0.8mm，所以我们图形的最小切割线条应该是比较0.4mm宽。
* 电线最好不要走直角，而是45度角。
* 电线与电线之间的距离也不能太近，需要平衡。
* 把5v和GND的电线都画得宽一些，我这里都做成了0.6mm。默认的电线是0.254mm  

完成了电路板之后，我会在AI里进行调整，比如加上边框、写上pcb的名字等。   
最终我导出了三个非常清晰dpi999的png。分别是pcb的洞、边框和只需要切割铜层不切穿透的部份。
我为它绘制了一个像面包一样的边框，在切割的时候我也发现了一些问题。  
![toastinohalf-01](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/ab70fcff-726c-4e56-8c66-04807c3ff103)  
![holestoastino-01](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/752e9f48-6198-47f0-a760-1214ce5bc2f6)  
![toastino-01](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/f2ae909e-5d26-448c-8c46-78b2076cb57c)  
接下来你可以带着你的png来到这个网站
*https://modsproject.org*  
面包的边框与png文件的最大边缘重合，导致这个网站在生成切割文件的时候没有将边框的四周围连起来。因此，我重新制作了一个连起来的图片。  
点击open program，来到机器对应的文件
<img width="314" alt="截屏2023-10-26 12 51 47" src="https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/51e41b3f-3a9e-4e41-9142-065d8f402a0a">




## Assignment's description
Describe the assignment

## Documentation
Describe the work you did to complete the assignment

bullet point list
* item one
* item two
* item three

numbered list
1. item one
2. item two
3. item three

**bold text**

*italic text*

***italic and bold text***

example of an external link

[description of the website](https://www.https://www.example.com/)

example of a picture hosted on an external website

![picture description](https://djmag.com/sites/default/files/storyimages/Clara_Rockmore.jpg)

example of a picture hosted inside your repository (don't forget the ./ operand)

![picture description](./images/example.jpg)
