# yet-another-soil-moisture-sensor

## A battery powered soil mositure sensor

## Overview

A project to learn something about electronics/esp32/home automation while keeping your plants and/or garden watered.  It probably suits a hobbyist, or a high school. It may not be the ideal "first" esp32 project but with the addition on an led you have all the kit you need to get a reasonable handle on esp32's and basic electronics. 

## Features

- Battery powered with battery monitoring and infrequent charging
- Home assistant integration

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

Notes on hardware. In 2025 this project might cost you AU$60 or more if you don't already have some bits.  While the heart, the esp32, might only cost you AU$9 and the sensor AU$3 the rest adds up and a waterproof polycarbonate enclosure can be AU$30.  Many of the above can be bought in packs.  I have included links to one supplier I use for my convenience.  You can use many of the various esp32 boards, I chose the c6 because it has both an onboard antenna and a 

## Tools
- Soldering iron
- Solder
- Optionally, phillips screwdriver and long nose pliers

  


Simple wiring diagram or Fritzing sketch if available.

Software / Setup / Installation

Steps to flash the ESP32 (e.g., Arduino IDE, PlatformIO, ESPHome).

Any dependencies or libraries needed.

Example:

git clone https://github.com/username/project.git
cd project
platformio run --target upload


Configuration / Usage

How to connect Wi-Fi, MQTT, or calibrate sensors.

Example configuration file snippet.

Screenshots / Demo (optional but engaging)

Terminal output, dashboard screenshot, or a photo of the running device.

License

A short line linking to your LICENSE file.

Example: This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Acknowledgements / Credits (if needed)

Shout-outs to libraries, tutorials, or people that helped.
