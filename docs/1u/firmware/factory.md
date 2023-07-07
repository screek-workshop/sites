Firmware recovery is limited to special cases where it is used as a last resort to restore the sensor to normal operation, which may include:  
- Long-term failure of the wiring, esphome saves a fixed wiring information in one location, ota also saves these settings, and the only way to clean them is to recover the firmware. This effect can also be achieved by clicking factory reset in the web page where you can access the firmware. But the ota update will not overwrite the settings.  
- The firmware is corrupted, or the DIY firmware fails to write, etc.  

## Factory Firmware File
### V2023_0704_1
We have made a number of improvements to the stability of 1U:  

- Reduced the update strategy for some debug parameters  
- Lowered the main frequency, reducing 240Mhz to 80Mhz, which our tests found to be fast enough for a task like radar. This is even better for temperature and persistence stability.  
- Improved the Wifi signal strategy, removing the overly aggressive one.    

**Downloads**  

[Factory-V2023_0704_1](files/factory-screek-humen-sensor-1u-20230704_1.bin){ .md-button .md-button--primary }

## How To Use

!!! info
	This is an advanced topic that requires some knowledge of esp32. If your sensor is running properly, you usually don't need to do this. Normal firmware updates can also be run via OTA.

Due to the special nature of S2 Mini, it is not possible to write words in web.esphome.io. You need to use some specialized tools to write to:
- Flash Download Tools for Windows, by ESPRESSIF: [link](https://www.espressif.com/en/support/download/other-tools)
- Esptool, A command line tool for Python.[Install](https://docs.espressif.com/projects/esptool/en/latest/esp32/installation.html), [doc](https://docs.espressif.com/projects/esptool/en/latest/esp32/esptool/basic-commands.html).

Regardless of which tool you use, you may need to be in the right mode to write to the recovery firmware::  
- If the sensor is running normally, you can hit swipe write twice and it will reboot and jump into bootloader mode. Due to the limitations of the S2, you will select the serial port again and write.
- If the sensors are not running properly, or the above method does not work for you, you use open the sensors, keep button 0 of the development board pressed and press button RST. If you know where they are, you can do it without opening the box, through the small hole on the side, but that will be a bit more complicated.  

The firmware write address is from 0x0, regardless of the tool.  

!!! tips

	After writing the firmware in DFU mode is finished, the device will not reboot automatically due to S2 limitations, you need to reboot manually: if the motherboard is turned on, you can press the RST button. You can also unplug it again and plug it in. This is done with the help of powering up.  

### Terminology
- factory: The factory firmware, which includes the bootloader, the setup area, will overwrite everything.
- dfu: (**Development Firmware Upgrade**)A special device update mode in which a thorough operation can be performed with minimum interference.