# DIY V1.0 ARDUINO UNO [under-construction]

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

![](https://upload.wikimedia.org/wikipedia/commons/3/38/Arduino_Uno_-_R3.jpg)

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

# make an Arduino

Ok, so first let’s decide what components we need? We must have the ATMega328-p microcontroller. We could have that in an AU or PU format. I’ll use PU format with a socket since I might want to remove the chip sometime.
Ok, the microcontroller can’t work by itself. It needs the bare minimum configuration in order to work. This is all it needs to work.
make an Arduino ATMega328 bootloader

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
