# Open MQTT Gateway - LoRa Sensors

This is a modified version of Open MQTT Gateway.  This is part of a LoRa mailbox sensor project that you can find more details about [here](https://tommyjlong.wixsite.com/home1/post/lora-mailbox-sensor-for-home-assistant).

OMG has been modified to use OMG's "ValueAsATopic" capability for LoRa sensors that provide a node-id in their JSON message payload.  "ValueAsATopic" is a configurable item in OMG that, when enabled, allows some "value" in the payload received from a sensor to be tacked onto the end of the MQTT topic as a subtopic.  This "ValueAsATopic" however does not exist in OMG for LoRa based sensors, so modifications were made to OMG that would allow it to parse the node-id from the message and tack it onto the MQTT topic.  For example, if the node-id is 12345678, the MQTT topic will now look something like: <br/>
` /home/OpenMQTTGateway_ESP32_LORA/LORAtoMQTT/12345678`

Modifications were also made to make use of a LILYGO TTGO v1 OLED display.  When the OMG first boots up, it will display a simple message saying the LORA GW is Ready, and later on will display the LoRa message it received from a LoRa Sensor. 

Finally, there are a couple of 3D printed parts that are available for the LILYGO TTGO v1 OLED display and its antenna.

# Credits
* Open MQTT Gateway.  
  You can find more details by going to there github repository [here](https://github.com/1technophile/OpenMQTTGateway) as well as their community forum here: 
  [![Community forum](https://img.shields.io/badge/community-forum-brightgreen.svg)](https://community.openmqttgateway.com)
* 3D Printed Part for Lilygo TTGO <br/>
  The 3D part originated from [Neodyme at Thingiverse](https://www.thingiverse.com/thing:3771284), but I heavily modified it so that the top side could more easily fit into the casing, and I changed the antenna orientation too.
