---
layout: post
title: "Getting Started with MicroView"
category: intro 
tagline: by JP Liew
description: "Step-by-step instructions for setting up the Arduino software and connecting it to your MicroView."
thumbnail: /images/Thumbnail_MicroView_Getting_Started.png
tags: [microView, setup, getting started, codebender, arduino ide, microview library]
comments: true
---
In order to get your MicroView up and running, there are four easy steps to follow: 

1.  Prepare MicroView for programming
2.  Choose Arduino software
3.  Select the right board
4.  Run your first sketch

#STEP 1 - Prepare MicroView for Programming

Once you have finished the FTDI Drivers installation, you will need to prepare your MicroView to be inserted into the computer's USB port.

If you have purchased the [factory USB Programmer]( https://www.sparkfun.com/products/12924), just insert the MicroView into the USB Programmer following the photo below.  Please take note that at the back of MicroView, there is a round dot marking showing the Pin 1 of the MicroView where you need to match the Pin 1 of the USB Programmer.

![MicroView Factory USB Programmer](/images/MicroView_Factory_Programmer.jpg)

Once you have inserted the MicroView into the USB Programmer, you can now insert the USB Programmer into the USB port of the computer as below.  If your computer does not have a right-sided USB port, please use a [USB Cable Extension](https://www.sparkfun.com/products/517) to extend the USB port to the front so that you can easily work with the MicroView.

![MicroView USB Programmer Connects to Computer](/images/MicroView_Programmer_To_Computer.jpg)

If you have not purchase the factory USB Programmer and have a [FTDI Basic Breakout -5V](https://www.sparkfun.com/products/9716) or [FTDI Cable 5V]( https://www.sparkfun.com/products/9718) lying around, they can also be used as a MicroView programmer. Connect the FTDI Basic Breakout board as below, and you are ready to go.

{% img /images/MicroView_FTDI_Programmer.svg 700 MicroView FTDI Basic Programmer Connection %}

<p class="success">You have now successfully prepared the MicroView for programming.</p>

#STEP 2 - Choose the Right Arduino Software (IDE)

There are currently two options when selecting the Arduino Sofware (IDE). The first option is to use the cloud based [Codebender](https://codebender.cc?referral_code=7fuuEtc89N) and the second option is to use [Arduino IDE.](http://arduino.cc/en/main/software)

<p class="info">As our Learning Kit's tutorials are based on Codebender, and Codebender has already included MicroView's library in their cloud solution, we highly recommend users to use Codebender for our tutorials. Plus Codebender has made the drivers installation really straight forward and easy.</p>

##Using Codebender

Installing Codebender is really simple, the prerequisite is just a Chrome or Firefox web-browser.  Using Chrome or Firefox, browse to [Codebender's Getting Started page](https://codebender.cc/static/walkthrough/page/1?referral_code=7fuuEtc89N) and then follow the steps below (shown using Firefox).

![MicroView install Codebender Step 1](/images/Codebender_Step01.png)

Click `Let's Go!`

![MicroView install Codebender Step 2](/images/Codebender_Step02.png)

Click `Add to Firefox.`

![MicroView install Codebender Step 3](/images/Codebender_Step03.png)

Click `Allow` when you see the message "Firefox prevented this site (codebender.cc) from asking you to install software on your computer."

![MicroView install Codebender Step 4](/images/Codebender_Step04.png)

Wait for the `Add-on downloading` to finish.

![MicroView install Codebender Step 5](/images/Codebender_Step05.png)

Click `Install Now`

![MicroView install Codebender Step 6](/images/Codebender_Step06.png)

Click `Restart Now` when you see the message "Codebender.cc Plugin will be installed after you restart Firefox."

After restarting, the browser will load up a Driver Installation page.

![MicroView install Codebender Step 7](/images/Codebender_Step07.png)

Click `Download Drivers` and save the driver zip file in your prefered folder. When the download is finished, click to open the zip file and then execute the driver installation file.

After the drivers have been successfully installed, a success page will be displayed.

![MicroView install Codebender Step 9](/images/Codebender_Step09.png)

<p class="success">You have now successfully installed the Codebender plugin on your browser. Please proceed to STEP 4 – Run Your First Sketch</p>

##Install Arduino IDE

Before installing Arduino IDE, it is recommeded to install the USB programmer's driver first.

###Install Drivers
MicroView, like the Arduino, relies on a programmer to upload sketches (Arduino code) and also communicate with the computer. This programmer often has a USB to TTL converter chip that creates a Virtual Serial Port on the computer when properly installed.  MicroView's [factory USB Programmer]( https://www.sparkfun.com/products/12924) uses the [FTDI's FT231X](http://www.ftdichip.com/Products/ICs/FT231X.html) to send the sketches to MicroView and also act as a communication medium between MicroView and the computer.

Depending on the OS (Operating System) of your computer, the drivers are installed using different methods.  Below are the installation instructions prepared by SparkFun Electronics:

* [How to Install FTDI Drivers for Windows]( https://learn.sparkfun.com/tutorials/how-to-install-ftdi-drivers/windows---quick-and-easy)
* [How to Install FTDI Drivers for Linux]( https://learn.sparkfun.com/tutorials/how-to-install-ftdi-drivers/linux)
* [How to Intall FTDI Drivers for Mac]( https://learn.sparkfun.com/tutorials/how-to-install-ftdi-drivers/mac)


###Install IDE
Installing the Arduino IDE is normally straight forward, however it is still a bit challenging if one has never try before.  Luckily our partner SparkFun have already published step by step guides on:

* [Installing Arduino IDE for Windows](https://learn.sparkfun.com/tutorials/installing-arduino-ide/windows)
* [Installing Arduino IDE for Mac](https://learn.sparkfun.com/tutorials/installing-arduino-ide/mac)
* [Installing Arduino IDE for Linux](https://learn.sparkfun.com/tutorials/installing-arduino-ide/linux)

<p class="info">After installation of the Arduino IDE has completed, unlike Codebender, you will still need to install MicroView's library.</p>

###Install MicroView Library

Download MicroView's library from our Github repo below:

[MicroView Library Github Repo](https://github.com/geekammo/MicroView-Arduino-Library/archive/master.zip)

Save the ZIP file to your download folder then unzip the ZIP file. Rename the folder name from `MicroView-Arduino-Library-master` to `MicroView`.

![MicroView Rename Library Folder](/images/MicroView_Rename_Library_Folder.png)

Open the Arduino IDE, click Sketch, Import Library and then Add Library.

![Add MicroView Library to Arduino IDE](/images/MicroView_Add_Library.png)

Browse to the `MicroView` folder that was renamed and select that folder.  The MicroView library will be automatically installed.

Click File, Example, and find MicroView Example to confirm the installation.

![MicroView Library Installed](/images/MicroView_Library_Installed.png)

If you wish to compile and upload the MicroViewDemo from out example, there is a 3rd party Time library that is required to be installed.  [Download the Time library](http://www.pjrc.com/teensy/arduino_libraries/Time.zip) and use the same method as installing a library discussed above to install it into the Arduino IDE.

<p class="info">The Arduino IDE requires users to manually manage and install 3rd party libraries, for a ready to go development environment, we recommend Codebender.</p>  

#STEP 3 - Select the Right Board

If you are using Codebender, the MicroView is fully supported and will be automatically selected in all our examples. Proceed to STEP 4 and click `Run on Arduino` to run your first sketch.

In the Arduino IDE, click Tools, board and select Arduino Uno. Click Upload to upload your first sketch to MicroView.

<p class="info">MicroView is using the same bootloader as Uno. It behaves like an Uno when uploading sketches.</p>

For advance user that like to see MicroView as a board by itself in the IDE, add the following board definition to the `boards.txt` file. Depending on your setup, the `boards.txt` file usually located at `arduino-version\hardware\arduino` folder. Replace `arduino-version` with the right folder name for your Arduino version installed in your computer.

    uview.name=MicroView
    uview.upload.protocol=arduino
    uview.upload.maximum_size=32256
    uview.upload.speed=115200
    uview.bootloader.low_fuses=0xff
    uview.bootloader.high_fuses=0xde
    uview.bootloader.extended_fuses=0x05
    uview.bootloader.path=optiboot
    uview.bootloader.file=optiboot_atmega328.hex
    uview.bootloader.unlock_bits=0x3F
    uview.bootloader.lock_bits=0x0F
    uview.build.mcu=atmega328p
    uview.build.f_cpu=16000000L
    uview.build.core=arduino
    uview.build.variant=standard


#STEP 4 - Run Your First Sketch

If you have installed Codebender, select the right COM port and then click `Run on Arduino` to upload your first sketch to MicroView. Watch the TX (red) and RX (yellow) LED blinks while the sketch is being uploaded to the MicroView.

<iframe style="height: 510px; width: 100%; margin: 10px 0 10px;" allowTransparency="true" src="https://codebender.cc/embed/sketch:38829?board=MicroView" frameborder="0"></iframe>

<p class="info">Arduino IDE users just need to cut and paste the above sketch starting from #include .... to ... void loop () {} into the Arduino IDE and click upload.</p>

<p class="success">Well done! You are now ready to try our other tutorials.</p>
