Xreceiver
==========
My own implementation of standalone XBOX360 wireless controller receiver, made of XBOX360 FAT RF Module and ATTiny13 (but it can actually be any AVR chip).

At first I used my development board with ATMega16 and wrote firmware, which received commands via UART and sent them to RF module, and it worked without any problems, you can find link to demonstration video in the end of the page. Then I decided to use more suitable microcontroller for it, my choice was ATTiny13 just because I had some of them. I decided to use power button on RF module to perform actions, which are pretty simple - short press to start  sunchronization with controllers, long press do power off all connected controllers.



List of required parts
------------
1. First of all, you need RF module itself. I used one with revision F, which worked fine wor me on Windows 7 and Mac OS (as I know, revision A has less reception range and has compatibility issues with Windows 8/10)
2. AVR microcontroller. Firmware is really simple and can be compiled with GCC AVR for any AVR chip, you may have to change CPU clock and GPIO mappings, the rest of code is universal. In "default" folder you can find compiled hex for ATTiny13 with stock fuses
3. Any 3.3 volts stabilisator, I used 1117-33
4. 2 filtering capacitors, I used 1 mF ceramic ones
5. 3 pulup resistors, I used 10K ones
6. Some USB connection - I used a cable with USB-A connector
7. Mounting wire, soldering iron, AVR programmer - as usual

Connection schematic
--------------
![Schematic](https://github.com/arch2saint/Xreceiver/blob/master/schematic.png)

Links
-----------
Demonstration of my first prototype
<https://youtu.be/K3Su9i-esuY>

The most usefull page with pinout and commands
<https://tkkrlab.nl/wiki/XBOX_360_RF_Module>

My thread on HackFAQ
<http://www.hackfaq.net/community/index.php?threads/15519/>

Another related articles
<https://gr33nonline.wordpress.com/2015/09/19/make-an-xbox-receiver/>
<https://www.se7ensins.com/forums/threads/how-to-make-a-homemade-xbox-360-controller-wireless-receiver-for-pc.668839/>
