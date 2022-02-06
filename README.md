# How-to-build-Arduino-on-bread-board

![image](https://user-images.githubusercontent.com/19898602/152667122-e01a5c1f-3b1d-4582-a9f2-d0d9ec9846f1.png)


If you are like and me and enjoy building electronic projects then you might have worked with the Arduino Uno. 

The Arduino uno is the most popular micro controller of the series and has a large collection of libraries which make working with it very easy. 

So there would be times where you may need more than one Uno for the project, I like to make my own micro controller rather than buying a new one, 

as this saves me some money which may be helpful for other such projects.

In this tutorial I'm going to show you how to, build your own Arduino Uno clone, so you can use it along side with circuits. 

This is a breadboard tutorial so no soldering skills are required.

# Components Required

![image](https://user-images.githubusercontent.com/19898602/152667129-4cea9074-cacf-42a2-8616-d6ec3c0e1fa3.png)

USB to Serial module (you can also use an Arduino Uno if you have one)

> Atmega328 IC
> 16 Mhz Crystal
> 22pF Capacitor
> L7805 Voltage regulator
> 10uf Capacitor
> LED
> Breadboard
> Connecting Wires
> 6V or 9V or 12V Power supply
> Soldering Iron


# Atmega328

![image](https://user-images.githubusercontent.com/19898602/152667152-64b2acf5-27cc-4d8b-9e74-d0801cb73ac2.png)


The Arduino is based on the Atmega328 IC and it is also the heart of the circuit. All the processing and everything else is done by the IC. The Atmega328 has to have a arduino boot loader flashed on to it to program it using the Arduino IDE.

The arduino uno is made of three parts

> Atmega328 IC
> Voltage Regulators
> Serial Programmer

  
You can purchase an Atmega328 IC with the Arduino boot-loader pre-installed or you can also install it yourself but you will need an Arudino uno to install the boot-loader. So it is recommended to get a Atmega328 with a pre-installed boot-loader.


# Voltage Regulator

![image](https://user-images.githubusercontent.com/19898602/152667168-b898cd58-034a-48d3-a503-c58be9fb0d15.png)
![image](https://user-images.githubusercontent.com/19898602/152667175-67ccd1d8-d393-4b7a-b46c-4d22371edb96.png)


The first step will involve building a voltage regulator, the atmega328 is a 5V micro controller so is the arduino Uno. So we need a regulated power supply to power the Atmega328 IC. For this we will be using a L7805 voltage regulator this is a popular voltage regulator and is cheap and serves the purpose of building an Arduino uno. This voltage regulator gives a voltage of 5V and a maximum load current of 1A.

You can also use a better efficiency regulator if you need more power output. You may also use a breadboard power supply as an alternative.



![image](https://user-images.githubusercontent.com/19898602/152667181-2d4b6d56-6fce-4f54-961c-ac8b80b0e9f9.png)

![image](https://user-images.githubusercontent.com/19898602/152667182-38e4ce87-43ed-441e-a23f-0e78c928bfce.png)

The circuit is fairly simple and the connections from the Arduino to any external circuit may vary depending on the external circuits. It would be recommended to try it out on a breadboard first. Follow the circuit above and assemble it on the breadboard. You can also add a led on digital pin 13 if you want to replicate the on board led as on the Arduino uno.

I am assuming you got an arduino with a preinstalled boot-loader if you got one without the bootloader you can use an Arduino uno to flash the boatload on the IC.


Before moving fuurther I would like to tell you something about PCB

Yes PCB are the heart of the electronics based project usually we hesitate to try custom PCB and opt to homemade solutions

like breadboard or Zero PCB earlier I also was in the same boat, I hesitate to try custom PCB my belief was they are much expensive.

but then I came to know about [JLCPCB.COM](https://jlcpcb.com/IAT) and I was totally surprised how low price PCB's are they offering 

there PCB quality is best in market, now I always go with PCB for my project and [JLCPCB.COM](https://jlcpcb.com/IAT) is my trusted 

PCB manufacturer, you can also try there PCB service for more details you can visit their website [JLCPCB.COM](https://jlcpcb.com/IAT)
You can also try there new purple colour for PCB without any extra cost.
If you get yourself registered today at [JLCPCB](https://jlcpcb.com/IAT ) you get coupons worth of 27$ from [JLCPCB](https://jlcpcb.com/IAT ).


![image](https://user-images.githubusercontent.com/19898602/134336832-cb9953e9-02a6-4ff7-9d27-2caad10fe7c7.png)
![image](https://user-images.githubusercontent.com/19898602/130722577-c30b7b43-ea89-4847-9c6b-058f9fabeda3.png)![image](https://user-images.githubusercontent.com/19898602/130722585-b5268db1-5f17-428f-ba60-b823140f2a70.png)



![image](https://user-images.githubusercontent.com/19898602/152667190-21500827-506e-429c-8077-83df5ae8b360.png)


In the atmega328 IC the pins 2 and 3 act as a serial port and to program the board all you have to do is connect these pins to the USB to serial converter. You can also use an arduino as an programmer to program the board. But using a USB to serial converter is much simpler to work with.

After you are done with the connections plug the USB end of the converter to a computer, and install the necessary drivers if you are on windows.


![image](https://user-images.githubusercontent.com/19898602/152667196-c0cf7a4a-8ef4-4e20-bfb8-43ba68a96470.png)


Before you can upload code to the board you need to download and install the Arduino IDE from the arduino official website. Then select the suitable serial port, board and you should now be ready to program your home made Arduino. To test the board you can try out the blink program you can find in the examples section of the Arduino IDE.

And you should now see the led connected to the digital pin 13 blink at an interval of every one second.


