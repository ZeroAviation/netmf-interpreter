## Visual Studio for NETMF Native Development

1. Download and install [Visual C++ for IOT Development](https://visualstudiogallery.msdn.microsoft.com/35dbae07-8c1a-4f9d-94b7-bac16cad9c01) extension
2. Navigate to `Solutions\STM32F746NUCLEO\VS` folder
3. To customize toolchain environment and msbuild options copy `build.props.user-example` to `build.props.user` and change the values of the respective properties
4. Open `STM32F746NUCLEO.sln` solution in Visual Studio
5. Select the **Release** configuration for **ARM** platform
6. Build

### Debugging

1. Download and extract OpenOCD - STM32F7 support requires version 0.10.x-dev, prebuilt binaries are availble at [Freddie Chopin's OpenOCD dev](http://www.freddiechopin.info/en/download/category/10-openocd-dev)
2. In Visual Studio select **Debugging** in the Project Properties and set the options for **OCD GDB Debugger**
    * _OCD Debugger Executable_ to `<GCC root>\bin\arm-none-eabi-gdb.exe`
    * _OCD Debugger Server Address_ leave `localhost:3333`
    * _OCD Debug Binary_ to `<NETMF root>BuildOutput\THUMB2FP\GCC5.4\le\FLASH\release\STM32F746NUCLEO\bin\TinyClr.axf`
3. Open command prompt in OpenOCD root folder and launch

`bin\openocd.exe -f scripts\interface\stlink-v2-1.cfg -f scripts\target\stm32f7x.cfg`

If the connection is successfully established, OpenOCD output should be
```
Info : STLINK v2 JTAG v27 API v2 SWIM v15 VID 0x0483 PID 0x374B
Info : using stlink api v2
Info : Target voltage: 3.238270
Info : stm32f7x.cpu: hardware has 8 breakpoints, 4 watchpoints
```
4. Switch back to Visual Studio and launch **OCD GDB Debugger** command (on the toolbar)
