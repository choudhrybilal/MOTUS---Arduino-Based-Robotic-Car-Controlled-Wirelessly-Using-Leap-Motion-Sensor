# MOTUS - Arduino Based Robotic Car Controlled Wirelessly Using Leap Motion Sensor

## Abstract

Motus is a robotic three wheeler vehicle built using 2-DC brushless 4 volt motors, Arduino UNO microcontroller, micro servo SG90 motor, caster wheel/directional wheel, and a turning mechanism controlled using Leap Motion Controller. The system can be consolidated into three components: Leap motion create VR-Virtual Reality environment, circuit proceeds and transmits signals, and the DC motors and servo motors provides the feedback. All signals transmit through the bluetooth module HC-05 connected to Arduino UNO microcontroller along with the laptop’s bluetooth. The system involves the use of both software and hardware. A 12 volt DC lithium ion rechargeable battery is the only source of power. The Motus enhances the human interaction with hardware experience in the real world.


### Step 01 
Configure the leap motion sensor using the following link below:
https://www.leapmotion.com/setup/desktop/windows

### Step 02
// Upload the file named 'EmptySketchFile.ino' to the microcontroller board (Arduino UNO)
#### Connect the HC-05 bluetooth module to the Arduino for configuration
We will program the Arduino to send AT commands to the module to configure it via a SoftwareSerial connection. Wire the TX and RX pins of your module to your Arduino. They need wired in a crossover configuration, so from the module to the Arduino wire TX to pin 10 and RX to pin 11. 

![alt text](BT_module_connection_1.JPG)

Then upload the following Sketch to your Arduino which creates a connection between the Arduino's serial port and the HC-05. Modify the ROBOT_NAME and the BLUETOOTH_SPEED values before uploading if you want a custom name or have changed the baudrate before. HC-05 has defaults baudrate (38400).

To put the HC-05 in AT commands mode you must connect the KEY pin in an arduino pin (I use pin 9) this is because this module works different.


