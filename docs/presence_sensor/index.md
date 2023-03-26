---
comments: true
---

This is a human body 24Ghz radar detector specially for HomeAssistant, which can detect moving human body as well as stationary human body. Based on HiLink's LD2410B(C) radar module, the module itself has Bluetooth function, and you can use HiLink's HLKRadarTool to adjust parameters very conveniently. Detectors are much smarter.

By combining the ESP32-C3 and the smart LD2410B to work together, and using the excellent and flexible ESPHome firmware, we can now make HomeAssistant easily sense the human body, and track distance and energy value changes easily through Bluetooth and the configuration APP (HLKRadarTool) combined with radar , allowing you to adjust the range of activities you want to perceive very flexibly and conveniently.

The sensor uses Type-C power supply, which is very convenient.

Using a well-designed 3D printed shell (designed by CSZ), it can be easily pasted on the wall, and the side with the Logo is facing the direction you want to sense. From then on, your HA can flexibly sense people coming and going up.

## Feature

- Use ESP32-C3 as a communication and data processing chip, It has better RF signal and better signal stability than ESP8266.High-quality WIFI signal, stability is the key factor to be a good sensor.We use the well-tuned ESP32-C3 module. The excellent RF tuning keeps the signal in a very good range, allowing it to capture the most timely information all the time.
- Well-tuned Esphome firmware, the signal is more stable, and it can make C3 work better.
- Support serial network configuration (improv_serial), This is currently a challenge for C3 support on esphome, we made some tweaks to make this possible.
- Quickly access HomeAssistant, automatically scan for new devices, and add them quickly.In the default firmware, your operation is very simple. We canceled the AP network configuration password, and also simplified the request for the API key in the connection process of HomeAssistant, so that you can find new devices in HomeAssistant so quickly and add it quickly, very convenience.
- Get the brightness of daylight by reading the photoresistor on the radar.This is a new firmware function of LD2410B, which will be available in the firmware version released in February 2023. We have made some fine-tuning to the official library to use the engineering mode to obtain the light sensor value output by the radar, which can roughly respond Changes in daylight. If you want ray data, it might be able to give you some help.

