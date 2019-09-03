# Displaying-Wireless-Temperature-Humidity-and-Temperature-Vibration-sensor-data-in-Node-RED-Dashboard

![alt tag](https://github.com/rjrajbir/Displaying-Wireless-Temperature-Humidity-and-Temperature-Vibration-sensor-data-in-Node-RED-Dashboard/blob/master/iot.jpg)

Measurement and monitoring of temperature, humidity, and vibration are very requested in great fields and areas such as health monitoring of systems. Currently, the use of these sensors is very recommended in health monitoring of systems due to the specifications of these sensors.
# Resources Required
- [IoT Long Range Wireless Temperature Humidity Sensor](https://store.ncd.io/product/industrial-long-range-wireless-temperature-humidity-sensor/) with power source Battery Or External DC.
- [IoT Long Range Wireless Vibration and Temperature Sensor](https://store.ncd.io/product/iot-long-range-wireless-vibration-and-temperature-sensor/) with power source Battery Or External DC.
- [900HP-S3B Long Range Wireless Mesh Modem with USB Interface](https://store.ncd.io/product/900hp-s3b-long-range-wireless-mesh-modem-with-usb-interface/)
- [Node-RED](https://nodered.org/docs/getting-started/installation).
- PC/Laptop with an OS installed or Any IoT Embedded Device.

Introducing NCD's Long Range variety of commercial IoT wireless Temperature/Humidity and Vibration/Temperature sensor, boasting as much as a 2-mile range using a wireless mesh networking architecture. Incorporating a 16-bit Vibration/Temperature sensor and a Temperature/Humidity sensor, these sensor transmits pretty accurate vibration, temperature and humidity statistics at user-defined intervals.

![alt tag](https://github.com/rjrajbir/Displaying-Wireless-Temperature-Humidity-and-Temperature-Vibration-sensor-data-in-Node-RED-Dashboard/blob/master/Ncd%20Tem_hum%20and%20vibration_tem%20sensor.png)

These sensors can be powered with 2 AA batteries and can work upto 500, 000 wireless transmissions, a 10 years battery life may be expected relying on environmental situations and the data transmission intervals.

Optionally, these sensors can be externally powered, making it a definitely best choice for wireless data tracking tool for the commercial equipment. Information can be transmitted to a PC, a raspberry pi, to Losant IoT cloud, Microsoft® azure® IoT, and an embedded machine all at the identical time.

To send these wireless sensors' data to any system as we discussed above, we need a [900HP-S3B Wireless Modem](https://store.ncd.io/product/900hp-s3b-long-range-wireless-mesh-modem-with-usb-interface/).

In this tutorial we are learning how to display these sensors data in Node-RED dashboard. So first of all we have to install Node-Red.

**Installing Node-Red**
Now you will be having your sensors in running mode, we need to use that data in efficient manner.

- At first of all, you’ll have to install [Node-RED](https://nodered.org/docs/getting-started/installation).
- Once it’s done, you need to start your command line, or Power Shell for Windows users, and then navigate the same to the directory where “Node-RED” is installed.
- Now type the command given below in your terminal.
```
npm i ncd-red-wireless node-red-dashboard   
```
- This will install the required nodes to receive data from your wireless sensors and you can start Node-RED once it’s done.
- To start node server, you need to write **node-red** in the command prompt or terminal and then press enter.
- Assuming at this point you’ve started up Node-RED, you should be able to open a browser and navigate to http://localhost:1880, this will open the flow builder that is the heart of the Node-RED experience.

[![Starting Node-red]()]()
