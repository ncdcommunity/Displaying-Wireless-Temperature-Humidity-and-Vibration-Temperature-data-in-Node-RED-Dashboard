# Displaying-Wireless-Temperature-Humidity-and-Temperature-Vibration-sensor-data-in-Node-RED-Dashboard

![alt tag](https://github.com/rjrajbir/Displaying-Wireless-Temperature-Humidity-and-Temperature-Vibration-sensor-data-in-Node-RED-Dashboard/blob/master/iot.jpg)

The manufacturing and production needs of 21's century global trade are growing at an extraordinary pace, developing commercial demanding situations that rely upon sensors for absolution. The trifecta of 24-hour international manufacturing needs, reliable real-time asset tracking, and the high aid value required to manipulate assets in far off places have led to the emergence of the economic IoT and its adoption of wireless sensors. Sensors are necessary for harsh business settings; the key lies in choosing the precise sensor.
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

![alt tag](https://github.com/rjrajbir/Displaying-Wireless-Temperature-Humidity-and-Temperature-Vibration-sensor-data-in-Node-RED-Dashboard/blob/master/Zigmo.png)

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

[![Starting Node-red](https://github.com/rjrajbir/Displaying-Wireless-Temperature-Humidity-and-Temperature-Vibration-sensor-data-in-Node-RED-Dashboard/blob/master/Starting%20node-red.JPG)](https://youtu.be/HC19BhuUrqs)

**Steps to build the flow**

- As you have started node-red, you'll be viewing a large blank flow with a list of nodes on the left side, which is known as palette.
- Now type **ncd** in search bar of the palette, go ahead and drag a Wireless Gateway node over to your flow canvas to get started.
**Finding your wireless Sensors**
- The next element we want to do is **configure** the node, when you first add it you’ll note that there is a small **triangle** at the top right corner, next to a **blue dot**, that triangle indicates that the node needs extra configuration, the blue dot indicates that the node has no longer but been deployed as part of the flow.
- Double click on the node to open up the configuration options.
- Click on the **pencil icon** next to the **Serial Device** field to configure your USB router, which will open the 2nd configuration panel that will be having a few options.
- Click on the **magnifying glass** next to the **Serial Port field** and select the port that corresponds with your router, then click the **“Add”** button on top.
- The serial device subject will now be populated based totally on that selection, and you may click **“done”**, you currently have direct access to your wireless sensors!

[![Starting Node-red](https://github.com/rjrajbir/Displaying-Wireless-Temperature-Humidity-and-Temperature-Vibration-sensor-data-in-Node-RED-Dashboard/blob/master/Finding_wireless_sensor.JPG)](https://youtu.be/oScbvN79vTw)

If you want to see the data that your wireless sensors are sending in, you can attach **debug node** to your wireless gateway.

**Working with the data**

Now out of your wireless sensors, data is gathered and it will be the output of the **“debug”** tab, this "debug tab" is placed on the right side bar which will be subsequent to the information tab. To see the information is available to hit the reset button. In node-red, records will be passed among nodes in a **JSON** packet. When the msg object comes into the debug tab you may make bigger it to view the overall list of information that comes with it. This will be useful in case you need to check that which all sensors are being added in. The other issue this node gives is an easy way to interchange your router to the network identity that devices in configuration mode document on, simply hit the button on the left of the node and the tool will switch to the configuration network, hit it once more to return it to listening mode.

**Adding the wireless sensors**
- Grab a **Wireless device** Node from the palette and drag it onto the flow, double click on it to get it configured.
- Click on the **magnifying glass** next to the Serial Port field and select the port that corresponds with your router, then click the “Add” button on top.
- Click on the **pencil icon** next to the **Serial Device** and **Serial Device for Config**, now fields will now be populated based on that selection.
- Select the Sensor as **Temperature and Humidity** or **Vibration** and click done.

[![Starting Node-red](https://github.com/rjrajbir/Displaying-Wireless-Temperature-Humidity-and-Temperature-Vibration-sensor-data-in-Node-RED-Dashboard/blob/master/adding_wireless_sensor.JPG)](https://youtu.be/-wi1_FXGzFE)

You’ll notice this automatically sets the sensor type for you, you can also give it a name to make it easier to identify.

**Node-RED Dashboard**
Provides the ability to create a **UI** using the flow builder, provides charts, graphs, and a number of other visual elements we can use to display data, along with nodes to trigger a flow using user input. We will use some of these nodes to display the data from your wireless sensors.

- Let’s check it out! There is a tab on the top right that says **“Dashboard”**.
- On the top right of that tab is the little **“new window”** icon, click on it to view your UI.

[![Starting Node-red](https://github.com/rjrajbir/Displaying-Wireless-Temperature-Humidity-and-Temperature-Vibration-sensor-data-in-Node-RED-Dashboard/blob/master/dasboard.JPG)]()

**OUTPUT**

![alt tag](https://github.com/rjrajbir/Displaying-Wireless-Temperature-Humidity-and-Temperature-Vibration-sensor-data-in-Node-RED-Dashboard/blob/master/output1.JPG)

![alt tag](https://github.com/rjrajbir/Displaying-Wireless-Temperature-Humidity-and-Temperature-Vibration-sensor-data-in-Node-RED-Dashboard/blob/master/output2.JPG)

**Applications of Temperature and Humidity Sensors**

- Warehouse Temperature Monitoring System
- Storage Unit Weather Monitoring System
- House Temperature Humidity monitoring
- Temperature Humidity Sensor for Device Control Applications
- Medical and Health Monitoring

**Applications of Vibration and Temperature Sensors**

- Machine Health Monitoring
- Ideal Device for Predicative Maintenance
- Future  Fail Detection and Alert System In Machines
