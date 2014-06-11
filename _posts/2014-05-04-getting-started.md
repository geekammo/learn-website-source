---
layout: post
title: "Getting Started with MicroView"
category: intro 
description: "Step-by-step instructions for setting up the Arduino software and connecting it to your MicroView."
tags: [microview, setup, getting-started]
comments: true
---

### Download Arduino Software (IDE) 

In order to get your MicroView up and running you'll need the latest version of the Arduino software available from the Arduino Website. The Arduino software (also known as the Arduino IDE), lets you program you MicroView (and other Arduinos). 

To get the Arduino software visit: [arduino.cc/en/main/software](arduino.cc/en/main/software).

### Install Drivers

Use the MicroView USB programmer or FTDI cable to connect your MicroView to one of your computer's USB ports. The MicroView USB programmer uses a special _FTDI chip_ to convert the signals from your computer's USB port into serial signals compatible with your MicroView. This _FTDI chip_ requires special drivers to be installed on your computer.


#### Installing FTDI drivers on Windows

#### Installing FTDI drivers on Mac

1. Head over to the FTDI site. Look on the left side for ‘Drivers,’ and then choose ‘VCP Drivers’.

2. Now we need to determine if you need the x86 or x64 bit version of the drivers. Click on the apple icon in the top left of the screen, and choose ‘About this Mac’.

3. Check under ‘Processor’ to see which version you have. Follow the chart below to determine which drivers to download.

4. Download the files from the site by clicking on the link. Locate the .dmg file that was downloaded to your computer, and double click on it. If you are not sure which version of OS X you have, use the same process as before when finding the processor type. Click on the apple and choose ‘About This Mac’. You will then see Version 10.X.Y–use the 10.X to determine your system version.

5. Continue through the installation, and wait for it to finish. Then click ‘Close.’


#### Installing FTDI drivers on Linux


### Identify Your Hardware

Your MicroView and the Arduino UNO are interchangeable but you won’t find the MicroView listed in the Arduino Software. Select “Arduino UNO” instead.

### Download and install the “MicroView Library”
