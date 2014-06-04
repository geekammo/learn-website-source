---
layout: post
title: "General Overview of MicroView"
tagline: by JP Liew
category: Intro
description: "General Overview of MicroView"
tags: [microview, introduction, overview, memory map, ssd1306, screen memory]
comments: true
---
![MicroView Image](/images/MicroView_Hero.jpg)

The MicroView is the first chip-sized Arduino compatible that lets you see what your Arduino is thinking using a built-in OLED display. In the heart of MicroView there is an ATMEL's ATmega328P, 5V & 3.3V LDO and a 64x48 pixel OLED display, together with other passive components that allow the MicroView to operate without any external components other than a power supply.

#Hardware Specifications    
* Display: 64x48 OLED Display
* Microcontroller: ATmega328P 
* Operating Voltage: 5V
* Input Voltage: 3.3VDC - 16VDC
* Digital I/O Pins: 12 (of which 3 provide PWM output)
* Analog Input Pins: 6
* Flash Memory: 32 KB
* SRAM: 2 KB
* EEPROM: 1 Kilobyte
* Clock Speed: 16 Mhz
* No other components required

#Pin Configuration
![MicroView pinout](/images/MicroView_pinout.png)

#OLED Memory Map
The [SSD1306](http://www.solomon-systech.com/en/product/display-ic/oled-driver-controller/ssd1306/) is the controller built-in the MicroView's OLED.  It has flexible yet complex segment and common drivers.  One requires vast knowledge on memory addressing in order to use the SSD1306 controller.

MicroView's library was written to wrap around the complexities of the SSD1306 controller, so that user can issue simple commands to control the display. Although the SSD1306 has a built-in RAM (memory) for the screen, when connected using the SPI method, ATmega328P is not able to read the RAM (memory) of the SSD1306. Therefore the software will not be able to manipulate the screen memory to perform mathematical operation on the screen memory.

MicroView's library overcome this by allocating a 384 bytes ( (64 x 48)/8 bits) of memory from ATmega328P as buffer. The library can now manipulates the buffer memory and then perform a bulk transfer from the ATmega328P's memory to the internal memory of the SSD1306 controller. 

The 384 bytes of buffer memory are declared in MicroView's library as

    static uint8_t screenmemory [] = {.total 384 bytes of data..};

and are arranged in a linear form representing the following 64 x 48 pixels coordinate system.

![MicroView Coordinate System](/images/MicroView_Coordinates.png)

Based on the above illustration, for example, if a user wish to plot a pixel at the position of the black dot, where X=10 and Y=2, user issue the following command:

    uView.pixel(10,2);

This command will then calculate the exact location of the buffer memory and set a BIT in the BYTE corresponding to the X,Y position.

![MicroView Memory Map](/images/MicroView_MemoryMap.png)
_Diagram showing how a linear buffer memory in the ATmega328P aligns with the OLED pixels._

![MicroView Data Bits](/images/MicroView_DataBits.png)
_Diagram showing the BITs in a BYTE of the buffer memory corresponding to the OLED's X,Y position._

Based on the above illustration, a pixel turned on at X=2 and Y=3 means BYTE 2 of the buffer memory has a data of 0x08 (hex). 

Two pixels at X=2,Y=3 and X=2,Y=2 turned on means BYTE 2 of the buffer memory has a data of 0x0c (hex).

To draw a straight line of 5 pixels starting from 10,2 to 10,2 , the following C codes show a simple way on how to accomplish this.

    uView.pixel(10,2);
    uView.pixel(10,3);
    uView.pixel(10,4);
    uView.pixel(10,5);
    uView.pixel(10,6);

In order for the library to perform extremely fast draw (more than 100 frames per second), all drawing function in the MicroView's library does not immediately transfer the buffer memory to the SSD1306 controller. A `display()` command is required to instruct the library to perform the bulk transfer from the buffer memory to the SSD1306 controller:

    uView.display();

This function take the whole buffer memory in the ATmega328P and transfer them via SPI bus (programmed at 8Mhz) to the internal memory of the SSD1306. As soon as the memory is being transferred, the pixels corresponding to the buffer memory will show up on the OLED.
