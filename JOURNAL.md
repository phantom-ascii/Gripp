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

# Oct 27 Finished the main board
That was much easier than i though making the pcb was actually so flipping easy it just took a while. i started by assignign footprints wihch may have been the hardest bit of this project using claude and firefox to find the footprints i need i then moved onto assignign 3d models. idk about you but i neeeeeed to assign 3d models to my components. Seeing an accurate 3 version of your pcb is just so satisfying. I then started with placement. I placed the 4 input keys in a cluster and the *shift key thing* sparatly on the right of the board. i put the xiao in the bottom left and out of the way so tracing would be easier and i pu the 4 servos output at the top of the board leavign sufficent space for the actual plastic headers to clip in. i put my screw terminal in the bottom left keeping it close to the other power components to keep the 2mm power traces short and simple:

![insert image here](https://github.com/phantom-ascii/Gripp/blob/main/images/6.png)

I think in the whole pcb i only used 2 vias wich i think is a flex. I then started by tracing which was easy enough. I sytarted with the main power rails such as vin and 5v (not gnd as i would have a gnd pour on the front and back copper) which were all 2mm width by using different netclasses. the rest of the tracks were 0.3 mm. I put all power rail tracks on f.cu and most other tracks on the b.cu. I ran a quick drc and fixxed a quick problem where my gnd fill was split into two islands. I fixxed it by just increasing the boards length tso the fill could go around traces and reach the other island as shown here:

![insert image here](https://github.com/phantom-ascii/Gripp/blob/main/images/7.png)

and got 0 errors on drc:

![insert image here](https://github.com/phantom-ascii/Gripp/blob/main/images/8.png)

final board traced:

![insert image here](https://github.com/phantom-ascii/Gripp/blob/main/images/9.png)
![insert image here](https://github.com/phantom-ascii/Gripp/blob/main/images/10.png)

I then snatched an image from pinterest for the desing on the back of the pcb and added the hack club orhpeus flag:

![insert image here](https://github.com/phantom-ascii/Gripp/blob/main/images/11.png)

I also added a bit of silkscreen on the front of the pcb:

![insert image here](https://github.com/phantom-ascii/Gripp/blob/main/images/12.png)

This is the final board:

![insert image here](https://github.com/phantom-ascii/Gripp/blob/main/images/13.png)

Then I used a kicad fabrication mod and generated the gerbers, drill files plotters ect and after a few git this git that committed everything to my github. *** ik i need to work on the read me ***
**Total time spent: 2 hours**
