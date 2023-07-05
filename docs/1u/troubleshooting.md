If you encounter some situations where you can't simply connect directly, here will be some suggestions.

## Cannot discover devices in Home Assistant

In most cases, as soon as the network is configured, the sensor broadcasts its own address and Home Assistant is able to discover the device automatically.    
  
However, some circumstances may affect this discovery process:    
- If the router blocks the devices from accessing each other, the devices are undiscoverable and cannot be connected. For example, the sensor is connected to an isolated guest network.  
- If a sensor has been added in Home Assistant, but then removed, it will not be discovered again at this point. This behavior is already present in Home Assistant version 2023.06.  
  
### Use USB cable and computer to configure network and view IP address

visit page: [https://web.esphome.io/](https://web.esphome.io/)

<figure markdown>
  ![](assets/Pasted%20image%2020230705132829.png)
  <figcaption>Click Connect Button</figcaption>
  
  ![](assets/Pasted%20image%2020230705133054.png)
  <figcaption>Select Loin S2-Mini Port</figcaption>

 ![](assets/Pasted%20image%2020230705133159.png)
 <figcaption>Select Configure Wi-Fi Button</figcaption>

 ![](assets/Pasted%20image%2020230705133322.png)
 <figcaption>Click CONNECt TO WI-FI</figcaption>

 ![](assets/Pasted%20image%2020230705133427.png)
 <figcaption>Select the name of your wireless network and if it does not appear, click the refresh button with the arrow in the upper right corner.</figcaption>

 ![](assets/Pasted%20image%2020230705133548.png)
 <figcaption>Enter the password to connect to the hotspot and click Connect</figcaption>

 ![](assets/Pasted%20image%2020230705133643.png)
 <figcaption>Wait a little while for it to finish mapping the network. Sometimes it won't work once, try twice more.</figcaption>

 ![](assets/Pasted%20image%2020230705133742.png)
 <figcaption>If successful you will see this page, click VISIT DEVICE and you will see the IP page where the device is located.</figcaption>

 ![](assets/Pasted%20image%2020230705133854.png)
 <figcaption>This page is the actual IP address of the device, and the presence of this page indicates that the sensor is working well.</figcaption>
 
</figure>