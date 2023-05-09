[![Version: 1.0 Release](https://img.shields.io/badge/Version-1.0%20Release-green.svg)](https://github.com/htl-rankweil/megacard) [![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

# Megacard

## Libraries

Easy to use libraries can be found in following directories

* [Libraries for ATmega16A integrated Hardware](./library/)
* [Libraries for External Hardware](./external/)

---

## Setup avrdude with Microchip Studio

Download Avr Dude [`avrdude-v?.?-windows-x64.zip`](https://www.microchip.com/mplab/avr-support/atmel-studio-7) and [Microchip Studio 7](https://www.microchip.com/mplab/avr-support/atmel-studio-7)

Copy avr-dude to a preferred path (e.g. `C:\Tools\avrdude`) and setup external tools in Microchip Studio 7.

![External Tools in Microchip Studio](./images/microchip-studio-external-tools.png)
![Setup AVR Dude in Microchip Studio](./images/microchip-studio-avr-dude.png)

``` bash
# Title
AVR Dude
# Command
P:\lehrer\GAR\Software\AvrDude\avrdude.exe
# Arguments         !PORT!
-c arduino -p m16 -P COM? -b 57600 -U flash:w:"$(TargetDir)$(TargetName).hex":a
```

> Important: It is necessary to setup the right COM-Port!

![Windows Hardware Manager](./images/win-hardware-manager.png)

---

## Software

Additional software that needs to be installed:

* [Microchip Studio 7](https://www.microchip.com/mplab/avr-support/atmel-studio-7)
* [TeraTerm](https://ttssh2.osdn.jp/index.html.en)
* [AVRdude](https://github.com/avrdudes/avrdude/releases)

---

**HTL-Rankweil**