---
title: "Gripp"
author: "phantom-ascii"
description: "A beutifully simple robot arm"
created_at: "2026-10-26"

# Oct 26 IK i started another project but welp

IDK why im started *another project* but oh well. I wanted to get a bit into robotics and what better way to dabble than to do. Anyways i want to make a rly simple robot arm that works... (none of my hardware projects so far have worked so welll yhhh). Also wanna see how well i can 3d model this cause my skills arnt that good... anyways heres a picture of what im trying to make

![insert image here](https://github.com/phantom-ascii/Gripp/blob/main/images/1.png)
@geeky-gadgets for the image

**Total time spent: 0 minutes**

# Oct 27 I have finished the schematics

WOW that took quite a while. I started the project i froze the mvp.I want a 4 axis simple robotic arm featuring the xiao rp2040 mcu. I also want 5 mx keys to control and switch modes of the actual arm. For the schematics i decided to separate it into nicely done 4 sections. i firstly started the power system using gemini to help and claude to check schematics. After going back and forth with the two ais i finally finished what i think is the finalized schematics. Luckily i got 0 errors on my erc on my *first try* (rly proud of that). I used gemini to mainly block out what i want in the actual schematics and what connects to what/ i then would send screenshots with context to claude so it could check for any errors missed by gemini. I found working with two ais is better than one so hallucination occurs less, one ai can fact check the other and if an ai is biased in a certain way the second ai will not follow those traits and will give unbiased opinions. 

Full Schems:
![insert image here](https://github.com/phantom-ascii/Gripp/blob/main/images/2.png)

MCU:
![insert image here](https://github.com/phantom-ascii/Gripp/blob/main/images/3.png)

Power:
![insert image here](https://github.com/phantom-ascii/Gripp/blob/main/images/4.png)

Input/Output:
![insert image here](https://github.com/phantom-ascii/Gripp/blob/main/images/5.png)

Im going to work on my PCB design next. I think doing the pcb before the actual 3d modeling is smarter so then i can build an enclosure and a model reflecting the actual pcb rather than estimated dimensions. However one thing i am worrying is that my pins are not ordered correctly, for example for my servos i have a 3 pin and i get a different layout (5v, gnd and data) every time i search it up so i just choose the most frequently used layout online. Im worrying about this alot cause my github.com/phantom-ascii/S.O-Dongle project had a similar bug and the oled would just fry itself if i used it. hopefully everything works tho. **Till next time!**

**Total time spent: 2 hours**
