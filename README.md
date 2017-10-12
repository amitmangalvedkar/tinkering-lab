# Tinkering Lab #  

## Introduction ##  
This session starts with a browser based simulator and proceeds next to an actual sensor connected to a simulator (Arduino Uno). Finally this device data-points are sent to IBM Watson IoT Quickstart dashboard.   


## Simulator ##  
This section shows how you can use the Simulator to show multiple data-points on Quickstart dashboard.  

1. Open the simulator link https://quickstart.internetofthings.ibmcloud.com/iotsensor/

2. Top right side provides the device id.

3. This simulator has 3 data points - temperature, Humidity and Object Temperature.

4. All these parameters can be either increased or decreased.

5. Click top right of simulator to see the parameters in a dashboard.

6. You can keep on toggling between the simulator and the dashboard.


## Microcontroller ##
The previous section made use of a simulator. In this section, we make use of a real microcontroller with sensors.  
_**(Note to protect the sensor, you may have to connect a pullup resistor between the microcontroller and the sensor)**_   

#### Arduino sketch code with MQ4 Gas Sensor ####   
This section explains how you can connect gas sensors MQ4 to Arduino.  

1. If Arduino sketch is not installed, download and install Arduino sketch program from the link  https://www.arduino.cc/en/tutorial/sketchConnect .  

2. Connect the Arduino Uno (or other  falvours of Arduino) to MacOSX / Windows / Linux using USB port.  

3. Download the lpg_gas_sensor.ino file.

4. Verify the code by clicking on the top-right tick mark.

5. Upload the code to the Arduino.

6. Disconnect the Arduino Uno from the development system.

7. Connect MQ4 Gas sensor to Arduino by connecting   
a. Vcc pint of Gas Sensor to 5V pin of Arduino  
b. Gnd pin of Gas Sensor to Gnd pin of Arduino  
c. A0 pin of Gas Sensor to A0 pin of Arduino

8. Connect the Arduino (with the Gas Sensor) back to the development system.  

9. Click on System Monitor and observe the readings.  



#### Arduino sketch code with DHT11 ####  
This section explains how you can connect DHT11 temperature and humidity sensors to Arduino  

1. If Arduino sketch is not installed, download and install Arduino sketch program from the link  https://www.arduino.cc/en/tutorial/sketchConnect .  

2. Connect the Arduino Uno (or other  falvours of Arduino) to MacOSX / Windows / Linux using USB port.  

3. Download the dht11_example.ino file.

4. Verify the code by clicking on the top-right tick mark.

5. Upload the code to the Arduino.

6. Disconnect the Arduino Uno from the development system.

7. Connect DHT11 to Arduino by connecting   
a. Vcc pint of DHT11 to 5V pin of Arduino  
b. Gnd pin of DHT11 to Gnd pin of Arduino  
c. A0 pin of DHT11 to A0 pin of Arduino

8. Connect the Arduino (with the DHT11) back to the development system.  

9. Click on System Monitor and observe the readings.  



#### Arduino sketch code with Ultrasonic sensor ####  
This section explains how you can connect Ultrasonic sensor to Arduino  

1. If Arduino sketch is not installed, download and install Arduino sketch program from the link  https://www.arduino.cc/en/tutorial/sketchConnect .  

2. Connect the Arduino Uno (or other  falvours of Arduino) to MacOSX / Windows / Linux using USB port.  

3. Download the ultrasonic_sensor.ino file.

4. Verify the code by clicking on the top-right tick mark.

5. Upload the code to the Arduino.

6. Disconnect the Arduino Uno from the development system.

7. Connect DHT11 to Arduino by connecting   
a. Vcc pint of Ultrasonic sensor to 5V pin of Arduino  
b. Gnd pin of Ultrasonic sensor to Gnd pin of Arduino  
c. Trigger pin of Ultrasonic sensor to D9 pin of Arduino
c. Echo pin of Ultrasonic sensor to D10 pin of Arduino

8. Connect the Arduino (with the Ultrasonic sensor) back to the development system.  

9. Click on System Monitor and observe the readings.  



## Node-RED Flow  ##   
This section shows how the connected Arduino device is made an IoT device by sending the events to Watson IoT Platform.  
1. In case Node-RED is not installed on the development system, install Node-RED by following the instructions given in the guide https://nodered.org/docs/getting-started/installation    
2. Add serial port node by following the instructions given in npmjs.com https://www.npmjs.com/package/node-red-node-serialport   
3. Add watson iot device by following the instructions given in npmjs.com https://www.npmjs.com/package/node-red-contrib-ibm-watson-iot   
4. Import Quickstart flow.  
5. Go to Quickstart dashboard and observe the events reaching the Quickstart dashboard.
