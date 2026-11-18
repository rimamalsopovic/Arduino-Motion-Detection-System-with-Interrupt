# Arduino-Motion-Detection-System-with-Interrupt

# Table of contents
1. Introduction
2. Components
2.1 Input and outputs
3. Algorithm Description
4. Block diagram
5. Connection schematic
5.1 Physical system connection
6. Flow chart
7. Conclusion

# 1. Introduction

With the integration of embedded systems in the modern-world, engineering solutions has permitted the automation of numerous processes which enriched both efficiency and convenience. Home alert security systems such as motion detection at the front door, is an example of this type of innovation.
This project demonstrates the design of a light and sound emmiting motion detection system which uses an Arduino Uno microcontroller as the central processing unit. It makes use of the PIR sensor to gather the data and determine whether or not there is movement within the predefined range of detection. In addition to this, there is a Piezzo buzzer and a LED diode. Each of them will respectfully emit a sound and light once movement is detected, signaling that motion has been detected.

 # 2. Components

Arduino Uno
Piezzo buzzer
LED
PIR motion Sensor
220 Ohm resistor
Breadboard
Jumper wires


# 2.1 Input and outputs

The input and outputs of this system are clearly defined in order to ensure proper operations. The former of the two, is responsible for the detection of any change within the environment, while the other presents a response based on the data provided by the input.

Input:
The PIR Sensor is used for the detecting any human motion within a specified range. This component is only used for gathering data which will later be used by the system to generate an alert. While it is searching for movement in its range, it will be sending either a LOW or a HIGH signal to present there is no motion or if there is one.

Output:
The buzzer makes use of the data provided by the input component previously described to generate a sound. This sound will be used as an alert to notify the individuals within the house that a person was detected outside.

The LED will emit a light once an individual is detected outside. It will do this by taking the data gathered by the PIR sensor.

# 3. Algorithm Description

When initialized, the Arduino Uno microcontroller beigns operations as it gets power to preform its operations. Following this, the remainder of the components are configured depending on their assigned pins. Once this is completed, the system will enter a monitoring stage. In this stage it will be searching for movements in a predefined range by using the PIR sensor. The PIR sensor will be collecting the data and send feedback to the Arduino Uno, thus infroming it if motion has been detected or not.

Once the PIR sensor detects movement it will send a HIGH signal to the Arduino. This signal represents the presence of a motion, be it done by a human or animal. When this signal is received the Arduino will in turn send a signal to both the LED and the buzzer. The LED will simply begin emitting a light which will serve as one method of notification. The second will the with the buzzer. As stated previously, the Arduino will send out a signal to the buzzer once the input has been processed. In the case that there is movement detected, the buzzer will let out a sound.

If there is no motion detected by the PIR sensor, it will send a LOW signal to the Arduino. This turn of events will not cause the Arduino to send out signals to neither the LED nor the buzzer. Without a signal being transmitted to either of these components they will not be informed to preform their specified tasks to inform that someone was detected by the system.

This system works in a constantly running if statement within a loop, with this continuous operation it guarantees to acuratelly detect motion at the front door. Once the PIR sensor detects motion it will send a HIGH signal to pin 2 which will halt the system's if clause and begin outputing sound and light. By making use of Arduino's incredible processing capabilities, the system is able reliably and acuratelly detect and infrom that there was a motion at the front door. With the additions of both the LED and the buzzer the user is properly notified. It they have impaired sight then they are still notified with the sound produced by the buzzer. However if the are not able to hear then the light of the LED will notify them that there is someone on the other side of the door.

# 4. Block diagram

Below is a block diagram of the previously explained system. As it can be seen below the PIR sensor will send a signal to the Arduino Uno microcontroller from the data it gathered. The microcontroller will in turn take this data and forward instructions to both the buzzer and the LED.

 
Figure 1. Block Diagram of Motion Detection System


 # 5. Connection schematic

All of the previously described components are connected using Jumper wires to the Arduino and Breadboard. With the PIR sensor having its signal connected to Pin 2 on the microcontroller. This was done for the purpose of implementing an interrupt within the program, this is described in further depth in the following segment of the report. The schematic for this project was made with TinkerCAD's circuit design. Below the connections are showcased:
Component	Connection
PIR VCC	5V direct
PIR GND	GND rail
PIR OUT	Pin 2
LED +	Pin 6
LED -	Resistor → GND
Buzzer +	Pin 12
Buzzer -	GND
 
Figure 2. Connection Schematic of Motion Detection System

# 5.1 Physical system connection

Below an image of the physical system powered off can be seen.
 
Figure 3. Physical system

# 6. Flow chart

The flow chart below how the system operates. Once it is started it will be checking if motion has been detected. If it has been detected then it will send a HIGH signal (the yes branch), in which the buzzer will produce a noise and the LED will emit a light. If there is a LOW signal (no branch) then the buzzer will remain silent and no light will be emitted from the LED. 
 
Figure 4. Flow Chart of Motion Detection System

# 7. Conclusion

This project is developed for the purpose of home security. The sensor is designed to detect motion and alert the inhabitants of the home. This is done with the system by having it emit a light and sound once motion is detected at the front door. The PIR sensor is used for the input detection while the LED and Buzzer are used for the above explained output. Various components are used to make the system, including an Arduino microcontroller, a Breadboard, a resistor, a set of Jumper wires as well as the previously mentioned components. 
The system works by using Arduino's pin 2 to send an interrupt once the PIR sensor senses motion. Once this is done the microcontroller follows the function within the code and procedes to interrupt the system's detection. When this comes to be the LED and buzzer will output to inform the client that someone is at the front door.
