## Firmware File
[Dropbox Link](https://www.dropbox.com/s/1nqeoqzv4vf8x1e/ota-screek-humen-sensor-1u-20230704_1.bin?dl=0)

## Whta't New
### 20270704_1
We have made a number of improvements to the stability of 1U:  
- Reduced the update strategy for some debug parameters
- Lowered the main frequency, reducing 240Mhz to 80Mhz, which our tests found to be fast enough for a task like radar. This is even better for temperature and persistence stability.
- Improved the Wifi signal strategy, removing the overly aggressive one.  

## How To Use

1. First we need to find the corresponding radar devices in HomeAssistant, they are often in Esphome, please note that we have modified its default name here. Click on the **VISIT** button, this will take you to the sensor's own web server interface.
![](assets/Pasted%20image%2020230704123535.png)


2. In the sensor's web server interface, which looks like this, select the file below:
![](assets/Pasted%20image%2020230704123717.png)

* Select an ota firmware:
![](assets/Pasted%20image%2020230704123930.png)

3. Click on the **update** button and wait for a while, depending on the network, it can be anywhere from a few seconds to tens of seconds.  

![](assets/Pasted%20image%2020230704124358.png)

![](assets/Pasted%20image%2020230704124340.png)
4. Return to HA's device page, refresh the page, and observe if the version information changes, and if it becomes the new date, then the update is complete.
![](assets/Pasted%20image%2020230704124505.png)