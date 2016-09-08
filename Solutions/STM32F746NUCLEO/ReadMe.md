# STM32F746NUCLEO Solution

This is a sample solution for STMicroelectronics NUCLEO-F746ZG board.

## Features

* STM32F746ZGT6 Cortex-M7 @216 MHz (max), 1 MB Flash, 320 KB SRAM
* On-board ST-LINK/V2-1 debugger/programmer
  * USB Mass Storage device for drag'n'drop programming
  * USB Virtual COM port (USART3)
* Three user LEDs
* Two push buttons: USER (blue) and RESET (black)
* USB OTG, USART/UART, I2C, SPI, ADC, DAC, CAN, GPIO
* Ethernet 10/100 Mbps

## Configuration

The Nucleo-144 board has numerous solder bridges (SBxx/SB1xx on top/bottom layer),
which are used to configure I/O pinout and various onboard features. Factory default
settings are assumed as described in the User Manual section 6.12.

[STM32F746NUCLEO.ioc](./STM32F746NUCLEO.ioc) is a baseline project file for [STM32CubeMX](http://www.st.com/content/st_com/en/products/development-tools/software-development-tools/stm32-software-development-tools/stm32-configurators-and-code-generators/stm32cubemx.html)
software configuration tool that allows configuring the required set of peripherals
via a graphical interface, with automatic conflict detection and alternate pin mapping
selection.

> _Note: The project is provided mainly for pinout and clock tree configuration,
> middleware features and C code generation are not used, so there could be some
> values missing or not set properly._

> _Note: Certain peripheral configurations are not possible due to limitations
> of the NETMF or because they are not yet implemented in the STM32F7 port drivers._

## Resources

* [NUCLEO-F746ZG - STMicroelectronics](http://www.st.com/content/st_com/en/products/evaluation-tools/product-evaluation-tools/mcu-eval-tools/stm32-mcu-eval-tools/stm32-mcu-nucleo/nucleo-f746zg.html)
  * [User Manual (PDF)](http://www.st.com/resource/en/user_manual/dm00244518.pdf)
  * [ST-LINK/V2-1 Firmware upgrade](http://www.st.com/content/st_com/en/products/embedded-software/development-tool-software/stsw-link007.html)
  * [ST-LINK/V2-1 USB driver for Windows](http://www.st.com/content/st_com/en/products/embedded-software/development-tool-software/stsw-link009.html)
* [NUCLEO-F746ZG - ARM mBed](https://developer.mbed.org/platforms/ST-Nucleo-F746ZG/)
  * Includes graphical board pinout


* [STM32F746ZG](http://www.st.com/content/st_com/en/products/microcontrollers/stm32-32-bit-arm-cortex-mcus/stm32f7-series/stm32f7x6/stm32f746zg.html?s_searchtype=partnumber)
  * [RM0385 - Reference Manual (PDF)](http://www.st.com/resource/en/reference_manual/dm00124865.pdf)
  * [PM0253 - Programming Manual (PDF)](http://www.st.com/resource/en/programming_manual/dm00237416.pdf)


* [LAN8742A Ethernet PHY](http://www.microchip.com/wwwproducts/en/LAN8742A)
  * [LAN8742A/LAN8742Ai Data Sheet (PDF)](http://ww1.microchip.com/downloads/en/DeviceDoc/DS_LAN8742_00001989A.pdf)
