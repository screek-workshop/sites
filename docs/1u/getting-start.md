The easiest way to get your device connected to Home Assistant to do its job is to use a hotspot to pair it with the network. You can use a phone, or a computer with a wireless network card to do this step.

## Prerequisites

In order to complete the networking process, you need to meet these conditions:    

- A smartphone capable of connecting to a wireless network, or a computer (can be a laptop, desktop computer, Mac computer, ChromeBook...) with a wireless network card.
- Your Home Assistant is connected to your local LAN, i.e. you can access it on your local LAN.  
- A stable and reliable 5V 1A+ USB power adapter for powering the sensor.  
- A Type-C data cable to connect the sensor to the power adapter. 

!!! info

	To make it easier to get started quickly, our accessories usually include a Type-C cable, and at least one double-sided adhesive.

## Configuring By A Smart Phone

In the demo below, we demonstrate using an iPhone to configure the device to connect to Home Assistant. if you are using an Android phone, the process is similar.  

!!! tips
	After connecting the sensor's hotspot, the phone will pop up a Configure Network page, 
	if it does not pop up automatically, please enter the page manually: [http://192.168.4.1](http://192.168.4.1).

<figure markdown>
![](images/phone_sel_network.jpg)
<figcaption>On the Select Hotspot page of the phone, select the hotspot for the sensor.</figcaption>

![](images/phone_save_pw.png)
<figcaption>After connecting the sensor's hotspot, the phone will pop up a Configure Network page, if it does not pop up automatically, please enter the page manually (http://192.168.4.1).Select a network hotspot for the sensor and enter the password.Click Save Button.</figcaption>

![](images/phone_wait_config_nw.png)
<figcaption>The device will start networking and if it goes well, the phone will disconnect from this temporary hotspot and go back to the original hotspot.</figcaption>

![](images/phone_setting_in_ha.png)
<figcaption>Click on Settings in the sidebar of HA</figcaption>

![](images/phone_device_in_ha.png)
<figcaption>Go in Device & Services</figcaption>

![](images/phone_config_btn_in_ha.jpg)
<figcaption>HomeAssistant will automatically discover your sensor and click Configure.</figcaption>

![](images/phone_submit_device_in_ha.jpg)
<figcaption>Click SUBMIT.</figcaption>

![](images/phone_finish_in_ha.png)
<figcaption>Click FINISH.</figcaption>

![](images/phone_device.png)
<figcaption>All Done! After the device is connected, you can find the device in the ESPHome integration and click 1 device to view the device properties.</figcaption>

</figure>