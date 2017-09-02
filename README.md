# ST7920-chipset LCD with Arduino test

This is a proof of concept for controlling an LCD dot matrix with an Arduino. The screen displays a spinning line. The wiring is quite neat and the code, when properly abstracted, will be easy to work with.

![spinning](spinning.gif "spinning")

## Hardware

* 128 x 64 LCD dot matrix display, with ST7920 chipset
* Arduino Uno

Any 128 x 64 LCD that uses the ST7920 chipset should work interchangably with this code, and similar chipsets may work equally well if the constructor is modified accordingly.

![wiring](wiring.png "wiring")

## Wiring

The wiring of the numerical pins (10, 11, 13, 8) can be changed however you wish - just change the pin definitions to match your setup. Obviously, the LCD pins that go to +5V/GND must go to those places.

LCD      | Arduino
---      | ---
`1  GND` | `GND`  
`2  VCC` | `+5V`  
`4  RS`  | `10`   
`5  R/W` | `11`   
`6  E`   | `13`   
`15 PSB` | `GND`  
`17 RST` | `8`    
`19 BLA` | `+5V`  
`20 BLK` | `GND`  

## Software

This code uses the [u8g2 library](https://github.com/olikraus/u8g2). This needs to be installed for the code to run. To install it, open the Arduino IDE, and navigate to `Sketch > Include Library > Manage Libraries...`, then search for "u8g2" and install it.

These pages from the u8g2 documentation will likely be useful to varying degrees:

* [Introduction to the library](https://github.com/olikraus/u8g2/wiki/setup_tutorial)
* [Constructor reference for ST7920](https://github.com/olikraus/u8g2/wiki/u8g2setupcpp#st7920-128x64)
* [u8g2 drawing api reference](https://github.com/olikraus/u8g2/wiki/u8g2reference)
