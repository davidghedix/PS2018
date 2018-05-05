# Pervasive systems - Personal project
![catturap](https://user-images.githubusercontent.com/24452470/39664949-35770a46-508c-11e8-8a1b-f7ea53d57d26.PNG)



This is a simple project to show the capabilities of Node-RED.
Goal of the project is to switch on or off a led remotely, from a smartphone or a laptop.
To accomplish this, two devices will be used: a NodeMCU and a Raspberry. 
NodeMCU acts as an MQTT client: it subscribes to topic «home/switchLed» and publishes to topic «home/ledStatus»
Raspberry Pi  is both an MQTT client and MQTT broker. NodeRED will provide:
  - A graphical interface to switch the led on and off
  - A log file that will be updated each time that the led is turned on or off

To interact with the led, it is required to open a web browser and connect to «yourIP:1880/ui/».


Note: if you want to switch on or off the led from an external network, you need to:

  - Change the firewall to allow inbound traffic on port 1880 
  - Set up a Network (and/or Port) Address Translation (NAT/PAT) entry that links requests from any address on port 1880, to 192.168.1.2       on port 1880.
  
Of course, security issues must be taken into account before doing this procedure.
