# DIY V1.0 ARDUINO UNO 
<pre>












https://github.com/Yasser-Jemli/MY_DIY_ARDUINO_UNO/issues/1#issue-1291484065



















</pre>



There are many versions of Arduino using the Atmega328 chip. 
There is the Arduino UNO, the NANO, 
the pro mini and other versions of boards that use the same chip.
For tests, when I’m building a new project, I almost always use the Arduino UNO because it is simple, it has female pins for me to connect jump wires,
it has a USB connector to program it,has external supply plug and voltages of 5 and 3,3 volts.
In this project, I’ve made my own unique Arduino UNO and name it MY_DIY_ARDUINO_UNO
, and I’ll show you how to make your own.
You, see, Arduino is an open hardware development board, all the components are free to buy and use, so,
I could gather all the components and make my own board and call it whatever I want. 
also through this project you will learn essential things about how microcontrollers work and what components are needed for them to work properly  



<pre>

<p align="center">
  <img width="460" height="500" src="https://upload.wikimedia.org/wikipedia/commons/3/38/Arduino_Uno_-_R3.jpg">
</p>

</pre>


# What do we need?

First of all, below you have a full part list for my design.
If you make your own using other components, 
make sure you use good and a low cost components. 
There are different options for the voltage regulator, 
FTDI communication adn so on...

Full part list:
<br /> 1 x ATMega328p- PU https://2betrading.com/arduino/228-atmega328-avec-bootloader-arduino.html . 
<br /> 1 x ATMega328p- PU SOCKET 
<br /> 1 x FT232RLSSOP 
<br />    OR: 1 x CH340 
<br /> 1 x AMS1117-5.0V https://2betrading.com/accueil/3180-module-ams1117-33v-regulateur-de-tension-ajustable-et-fixe.html . 
<br />    OR: 1 x MC33269DR2-5 
<br /> 1 x 16MHz crystal https://2betrading.com/quartz/3674-quartz-8mhz-8000mhz-dip-4.html . 
<br /> 1 x MINI-B USB conn https://2betrading.com/connectiques/2580-cable-usb-type-c.html .
<br /> 1 x smd push button 
<br /> 4 x female pins 
<br /> 1 x M7 diode 
<br /> 1 x 500mA fuse https://2betrading.com/fusible/2308-fusible-7a-125v.html .
<br /> 1 x smd switch 
<br /> 3 x 0805 LEDs 
<br /> 5 x 0805 1k resistor 
<br /> 1 x 0805 10k resistor 
<br /> 2 x 0805 22pF capacitor 
<br /> 3 x 0805 100nF capacitor 
<br /> 2 x 47uF SMD capacitor 
<br /> 1 x 0805 1uF capacitor 

Wire, soldering iron, solder, etc...

# original_schematic_of_an_Arduino_Uno


![](https://electronoobs.io/uploads/project_images/182/4c5bde74a8f110656874902f07378009_1.png)


# make an Arduino

Ok, so first let’s decide what components we need? We must have the ATMega328-p microcontroller. We could have that in an AU or PU format. I’ll use PU format with a socket since I might want to remove the chip sometime.
Ok, the microcontroller can’t work by itself. It needs the bare minimum configuration in order to work. This is all it needs to work.
make an Arduino ATMega328 bootloader

![Schematic_arduino uno_2022-06-13](https://user-images.githubusercontent.com/92098387/173309899-7fd499dc-1672-4fcc-847d-7c39195aeed7.png)

Now we have the bare minimum config on the breadboard and tested.
If you were able to uplaod code to it using the FTDI module, 
great. We can start with the project. Once this configuration works, 
you could make any board that you want.
Ok, now that we know the bare minimum configuration, 
let’s analyze the extra components the Arduino UNO has. 
First of all, as said before, 
I had to use and external FTDI chip to program the Arduino. 
My board will have that included. This chip makes the connection between the USB data and the ATMEGA328 so we could upload our sketches (programes) to the microcontroller. 
We also need a 5V voltage regulator, 
the USB plug and i will make a mini-USB because i just hate the USB-A that used in The ARDUINO_UNO ,
a reset push button, female pins all around, 
some extra capacitors, LEDs and a switch. 




   ![Screenshot from 2022-06-13 09-20-01](https://user-images.githubusercontent.com/92098387/173310860-e0f19d26-c005-4f27-9e1a-8b9238da8982.png)

# Burn The Bootloader


Now, if the chip doesn’t have a bootloader burned to it you should burn iNow make these SPI connections between the stock Arduino and your board. Once the connections are made, go to tools and select burn bootloader. The LEDs will start blinking very fast. Once you get the message bootloader successfully burned you are good to go. t first. Here is what you need to burn a bootloader to a new ATMEGA chip:

- Another Arduino UNO
- Some jump cables and
- USB cable

Connect the Arduino UNO to your PC and open ARDUINO IDE. Select Arduino board and go to examples ==> Arduino ISP ==> and open this example. Now upload this file to the Arduino UNO (original one). Now go to tools and change the programmer to Arduino as ISP. 

Now make these SPI connections between the stock Arduino and your board. Once the connections are made, go to tools and select burn bootloader. The LEDs will start blinking very fast. Once you get the message bootloader successfully burned you are good to go. 

![noobino_12](https://user-images.githubusercontent.com/92098387/174144200-5afe389b-bb0c-4182-8277-f0124ddebde7.png)
 

Connect the USB to your board, change back the programmer mode and upload a test sketch. There you go, I’ve made the LED blink with MY_DIY_ARDUINO_UNO  board. Pretty cool right?

This board works exactly like the Arduino UNO, but it is made just how I wanted or you want it . More male pins so less using of breadbored , SPI pads here and great color Remeber you can choose the color of your bored buy changing The Solder-Mask color and it depens on your manufacuture capabilities and the color of the solder mask they have. You can find all the extra information, schematics, gerbers and photos in this repository . So there you have it guys. 

# Installation 

you just need to go to the arduino website here : https://support.arduino.cc/hc/en-us/categories/360002212660-Software-and-Downloads
dowload the IDE, and that's it !! 
<br /> <p align="left"> <a href="https://www.arduino.cc/" target="_blank" rel="noreferrer"> <img src="https://cdn.worldvectorlogo.com/logos/arduino-1.svg" alt="arduino" width="40" height="40"/>
# Fabrication 

   
for the fabrication you can Upload the GERBER file that you will find in this repository and make the changes that you want in own Bored and make a Order 
Or if you are going to make it in a local Tunisian manufacture, you can simply  you can just contect 
   
<br /> <a href="https://linkedin.com/in/yasser-jamli-718582206/" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="yasser-jamli-718582206/" height="30" width="40" /></a>
<a href="https://fb.com/yasser.jemli.14/" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/facebook.svg" alt="yasser.jemli.14/" height="30" width="40" /></a>
</p>
  
  
  
me or you can delivery the Json files of the project 
Note : The json files are compatibile with EASYEDA 
