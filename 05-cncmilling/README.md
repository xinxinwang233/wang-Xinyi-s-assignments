# CNC

In this lesson, we will learn to sculpt a circuit board using an SRM-20 machine and drawing. I will record all the operation process below, and finally I have a DIY circuit board that can be used.
First, we use the platform to draw pcb drawings. 
*https://lceda.cn/*  
<img width="1621" alt="截屏2023-10-26 12 56 00" src="https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/e45c5f89-7fcc-437d-9820-831ff4256d60">  
We need to know the original packaging specifications we used, and we choose 1206 for all the packaging specifications.
<img width="868" alt="截屏2023-10-26 13 03 11" src="https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/1ccf2b67-5322-4b98-bf4e-e7121ae68064">  
After selecting all the originals, we only need to connect them with wires, here are some precautions.
<img width="270" alt="截屏2023-10-26 13 04 20" src="https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/3f3571af-b76e-4701-b3d5-4ace43957819">  

Connection considerations
* Need to know the size of the cutter head of the cutting machine, and in the drawing, there should be no shape smaller than the cutter head. This machine uses two pours, 0.4mm and 0.8mm, so the minimum cut line of our graphics should be comparatively 0.4mm wide.
* The wire is best not to go at a right Angle, but at a 45 degree Angle.
* The distance between the wire and the wire can not be too close, need to balance.
* Draw the 5v and GND wires wider, I have made 0.6mm here. The default wire is 0.254mm

After completing the circuit board, I will make adjustments in the AI, such as adding the border, writing the name of the pcb and so on.
I ended up exporting three very clean PNGS of dpi999. Respectively, the pcb holes, borders and only need to cut the copper layer does not cut through the part.
I drew a bread-like border for it, and I also found some problems when cutting it.
![toastinohalf-01](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/ab70fcff-726c-4e56-8c66-04807c3ff103)  
![holestoastino-01](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/752e9f48-6198-47f0-a760-1214ce5bc2f6)  
![toastino-01](https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/f2ae909e-5d26-448c-8c46-78b2076cb57c)  
Next you can bring your png to this site
*https://modsproject.org*  
The border of the bread overlaps with the largest edge of the png file, causing the site to generate the cut file without connecting the four sides of the border. So I re-created a connected picture.
Click open program to go to the corresponding file of the machine. At this time, you need to modify some parameters.
<img width="314" alt="截屏2023-10-26 12 51 47" src="https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/51e41b3f-3a9e-4e41-9142-065d8f402a0a">  
<img width="1592" alt="截屏2023-10-26 13 23 07" src="https://github.com/xinxinwang233/wang-Xinyi-s-assignments/assets/144413765/f60ddced-abf0-4f59-a682-6a990d28d26e">
Finally click calculate, the website automatically downloads the file.
We go to the machine, we upload the file to the machine,


