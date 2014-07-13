---
layout: post
title: "Quick Start"
category: intro
tagline: by JP Liew
description: "Step-by-step instructions to quickly start your MicroView."
thumbnail: /images/Thumbnail_MicroViewWithProgrammer.png
tags: [microView, setup, quick start]
comments: true
group: navigation
weight: 1
---
Thank you backing our Kickstarter project. Before we get underway with setting up your MicroView, you should make sure you have got everything you need. 

#Unboxing and setting up your MicroView

Remove all parts from the SparkFun packaging.

Identify PIN 1 of MicroView based on the following diagrams:

![MicroView PIN 1 diagram](/images/BreadboardWithMicroView.png)

![MicroView PIN identification](/images/MicroView_Factory_Programmer.jpg)

<p class="info">In this guide, when there is a reference for PIN x of MicroView, it is referring to the above diagram's PIN number. For example, connect PIN 5 and PIN 8 of the MicroView</p>

##MicroView without Factory USB Programmer
If you only have the MicroView without the USB Programmer, you will need the following:

* [9V Battery](https://www.sparkfun.com/products/10218)
* [9V Snap Connector](https://www.sparkfun.com/products/91) (Remove the Molex connector, replace both wires with male header pins if necessary)
* [Jumper Wires M/M Pack of 10](https://www.sparkfun.com/products/8431) (If you need more, you can also get the [Pack of 100](https://www.sparkfun.com/products/10897)
* [Breadboard](https://www.sparkfun.com/products/12002)

Connect the required parts based on the diagram below, leave the battery snap connector to the last step:

![Quick Start MicroView](/images/QuickStart_MicroView_Only.png)

As soon as the battery snap connector is snapped to the 9V battery, the MicroView demo will start.

##MicroView with Factory USB Programmer

If you have the factory USB Programmer, depending on your tier, you might need the following:

* [USB Extension Cable](https://www.sparkfun.com/products/517)
* [Breadboard](https://www.sparkfun.com/products/12002)

Insert the MicroView to the factory USB Programmer then connect the female end of the USB extension cable to the factory USB Programmer based on the following diagram:

![Quick Start MicroView with USB Programmer](/images/QuickStart_MicroView_With_Programmer.png)

Connect the male end of the USB extension cable to the computer, the MicroView demo will start.

#MicroView Teaching How To Use MicroView

The MicroView is factory pre-programmed with a few simple built-in tutorials to help you get use to inserting jumper wires, resistors and LED. Skip these tutorials  if you are already familiar with them. The simple tutorials will start after the demo. 

<p class="info">Note: The simple tutorials' diagrams are based on MicroView without the USB Programmer, if you have the USB Programmer, please ignore the battery, red jumper and black jumper.  MicroView with USB Programmer gets its power supply from the USB Programmer via the USB cable connected to the computer.</p>

##Simple Tutorial 1

Follow the instruction displayed on the MicroView, connect PIN 5 and PIN 8 of the MicroView with a jumper using the following diagram as reference:

![MicroView Quick Start Simple Tutorial 1](/images/QuickStart_Tutorial_1.png)

Once you have successfully connected PIN 5 and PIN 8 of the MicroView, a "Well done!" message will be displayed. To proceed to the next simple tutorial, remove the jumper.

##Simple Tutorial 2

Follow the instruction displayed on the MicroView, connect PIN 3 and PIN 8 of the MicroView with a jumper using the following diagram as reference:

![MicroView Quick Start Simple Tutorial 2](/images/QuickStart_Tutorial_2.png)

Once you have successfully connected PIN 3 and PIN 8 of the MicroView, a "Well done!" message will be displayed. To proceed to the next simple tutorial, remove the jumper.

##Simple Tutorial 3

Follow the instruction displayed on the MicroView, connect PIN 2 and PIN 8 of the MicroView with a jumper using the following diagram as reference:

![MicroView Quick Start Simple Tutorial 3](/images/QuickStart_Tutorial_3.png)

Once you have successfully connected PIN 2 and PIN 8 of the MicroView, a "Well done!" message will be displayed. To proceed to the next simple tutorial, remove the jumper.

##Simple Tutorial 4

Follow the instruction displayed on the MicroView, connect PIN 4 and PIN 8 of the MicroView with a 330 ohm resistor using the following diagram as reference:

![MicroView Quick Start Simple Tutorial 4](/images/QuickStart_Tutorial_4.png)

Once you have successfully connected PIN 4 and PIN 8 of the MicroView with the resistor, a "Well done!" message will be displayed. To proceed to the next simple tutorial, remove the resistor.

##Simple Tutorial 5

Follow the instruction displayed on the MicroView, connect PIN 4 and PIN 8 of the MicroView with a 10K ohm resistor using the following diagram as reference:

![MicroView Quick Start Simple Tutorial 5](/images/QuickStart_Tutorial_5.png)

Once you have successfully connected PIN 4 and PIN 8 of the MicroView with the resistor, a "Well done!" message will be displayed. To proceed to the next simple tutorial, remove the resistor.

##Simple Tutorial 6

Follow the instruction displayed on the MicroView, connect PIN 5 and PIN 8 of the MicroView with a 330 ohm resistor using the following diagram as reference:

![MicroView Quick Start Simple Tutorial 6](/images/QuickStart_Tutorial_6.png)

<p class="warning">With the resistor still at the same place, insert a LED with both of the pins at PIN 4 and PIN 5 of MicroView respectively using the following diagram as reference</p>

![MicroView Quick Start Simple Tutorial 6](/images/QuickStart_Tutorial_6_1.png)

The MicroView is able to detect if the LED is inserted with the correct polarity, if the LED does not blink, remove the LED and turn the pins the other way round and connect them to PIN 4 and PIN 5 of the MicroView. 

<p class="success">You have now successfully gone through our Quick Start.</p> 

Please proceed to [Getting Started with MicroView](/intro/getting-started.html) to install Arduino IDE or Codebender.
