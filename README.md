# yet-another-soil-moisture-sensor

## A battery powered soil mositure sensor

## Overview

A project to learn something about electronics/esp32/home automation while keeping your plants and/or garden watered.  It probably suits a hobbyist, or a high school. It may not be the ideal "first" esp32 project but with the addition on an [led](https://core-electronics.com.au/catalogsearch/result/?q=led+and+resistor+pack) you have all the kit you need to follow a [first project led blink esp32 tutorial](https://www.google.com/search?q=first+project+led+blink+esp32).

## Features

- Battery powered with battery monitoring and infrequent charging
- [Home Assistant](https://www.home-assistant.io/) integration

## Hardware

- [esp32-c6 development board such as Seeed Studio esp32-c6](https://wiki.seeedstudio.com/xiao_esp32c6_getting_started)
- [3.7v LiPo battery](https://core-electronics.com.au/catalogsearch/result/?q=2400mah%20LiPo)
- [Fuel Gauge such as Adafruit Max17048 Qwiic Fuel Gauge](https://core-electronics.com.au/catalogsearch/result/?q=Adafruit+MAX17048) and [Qwiic Cable if not included](https://core-electronics.com.au/qwiic-cable-50mm-41903.html)
- [Capacitive soil moisture sensor and connector lead](https://core-electronics.com.au/capacitive-soil-moisture-sensor-v20.html)
- [Headers for the esp32 and to connect the sensor to the board ](https://core-electronics.com.au/connectors-sockets/headers.html)
- [2-pin JST PH Connector cable](https://core-electronics.com.au/jst-2-pin-cable.html)
- [N-Channel MOSFET such as 2N7000](https://core-electronics.com.au/n-channel-mosfet-2n7000.html)
- 2 x 100Ω Resistors, 1x 10kΩ resistor,
- 26AWG wires (e.g. red, black, yellow)
- External antenna, such as [this](https://core-electronics.com.au/915mhz-ufl-antenna.html), if your esp32 supports an external antenna. (See notes.)
- [small protoboard](https://core-electronics.com.au/prototyping.html#category_60)
- Enclosure of [one type](https://en.wikipedia.org/wiki/Mason_jar#/media/File:Mason_jar_array.jpg) or [another](https://www.jaycar.com.au/search?q=enclosure)
- USB C cable for charging

Notes on hardware. In 2025 this project might cost you AU$60 or more if you don't already have some bits.  While the heart, the esp32, might only cost you AU$9 and the sensor AU$3 the rest adds up and a waterproof polycarbonate enclosure can be AU$30 making a jam jar look attractive.  Many of the above can be bought cheaply in packs for multiple projects.  I have included links to one supplier I use for my convenience.  

You can use many of the various esp32 boards, I chose the esp32-c6 only because it has both an onboard antenna and an interface for connecting an external UFL antenna. If you want to put the sensor in the garden where the WiFi might be weak then an external antenna will help.  

You can replace the sensor with any sensor that can interface with the [ADC](https://en.wikipedia.org/wiki/Analog-to-digital_converter) [GPIO](https://en.wikipedia.org/wiki/General-purpose_input/output)'s on the esp32. 

I started with a [voltage divider](https://en.wikipedia.org/wiki/Voltage_divider) to measure battery voltage.  While cheap this is basically rubbish due to the [discharge curve](https://www.grepow.com/blog/basis-of-lipo-battery-specifications.html) of LiPo batteries. The Max17408 provides a battery discharge percentage.  Some esp32/microcontoller boards have this built in.  

ESP32's can be placed into a deep sleep mode which draws very little current.  The [mosfet](https://en.wikipedia.org/wiki/MOSFET) allows the esp32 to also turn the sensor off saving battery. Because the soil moisture sensor uses very little current, it is ok to use a mosfet as a switch. (A relay is an alternative for higher current sensors and use cases.) Esp32's GPIO's [float](https://en.wikipedia.org/wiki/Floating_ground) when in deep sleep so the mosfet allows the esp32 to cut the power to the sensor. 

## Tools
- Soldering iron
- Solder
- Optionally, phillips screwdriver and long nose pliers

  


##  Wiring diagram



## Software 

This project is a [Home Assistant](https://www.home-assistant.io/) project because that makes it more fun and useful. (There are many tutorials out there with standalone soil moisture sensors with LCD or OLED or other displays.) 



## Installation

Example:

git clone https://github.com/username/project.git
cd project
platformio run --target upload


Configuration / Usage

How to connect Wi-Fi, MQTT, or calibrate sensors.

Example configuration file snippet.

Screenshots / Demo (optional but engaging)

Terminal output, dashboard screenshot, or a photo of the running device.

## License

This project is free to use under the [MIT License](https://github.com/bicycleboy/yet-another-soil-moisture-sensor?tab=MIT-1-ov-file).
