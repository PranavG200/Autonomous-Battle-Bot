# Autonomous Mobile Battle Bot

This project entails the development of a mobile autonomous robot with advanced sensing and communication capabilities right from its design inception to a fully working bot. The robot exhibits autonomous wall-following behavior, precise localization through Vive system integration, and employs infrared beacon tracking for targeted navigation. Notably, it communicates using communication protocols such as UDP and ESPNow, enabling dynamic interaction. The robot’s proficiency is demonstrated by its ability to autonomously manipulate objects, including grabbing a real trophy, pushing a fake trophy and a police car with precision, highlighting its adaptability in practical applications. This project was done as the part of the course MEAM510 : Design of Mechatronic Systems at University of Pennsylvania

<img width="494" alt="arch" src="https://github.com/PranavG200/Autonomous-Battle-Bot/assets/46398827/43732dc0-16f7-4dfa-9f17-b2b1a10a8e1d">

**Key Functional Components :**

*Sensing/Perception*

we integrated infrared sensors, employing detection circuits that utilized opamps and comparators to eliminate noise and precisely detect the frequency of emitted IR light. ultrasonic sensors were incorporated with software filters to refine readings, enhancing accuracy.

*Localization*

We employed HTC Vive which is a GPS-like localization system to precisely determine the robot’s position within its environment. we designed and implemented detection circuits for Vive’s tracking
sensors, gathering real-time data on its spatial coordinates. We performed calibration to ensure reliable and consistent localization To determine the robot’s orientation, a magnetometer was
utilized.

*Planning and obstacle avoidance*

we leverage the start position obtained from Vive localization and the end goal defined by either IR frequency recognition or Vive coordinates. Utilizing sensor inputs from infrared and ultrasonic sensors, we implemented reactive obstacle avoidance mechanisms to navigate around potential obstacles such as other vehicles and beacons.

*Control*

we implemented PID controllers for both lateral (angle/orientation) and longitudinal (distance) control. The desired distance and orientation, dictated by the planning module, guide the robot’s movements. 

*Web Interface design and communications*

For interface, we hosted a HTML based webpage and employed UDP WiFi communication, enabling interaction with the bot. The webpage featured task selection options, a stop button, and flags indicating task completion or timeout. Minimizing packet transmission was crucial. Additionally, we implemented ESPNow communication for seamless message transfer between the robot’s ESP microcontroller and the pilot microcontroller

<img width="712" alt="iso" src="https://github.com/PranavG200/Autonomous-Battle-Bot/assets/46398827/d2934bfd-f3f0-42a4-a064-9dcc37782b9b">

Bot Performing wall following -

[![Everything Is AWESOME](https://img.youtube.com/vi/<Lj7yCi2oDeo?si=GCSBrgnZZGK95ZWx>/0.jpg)](https://youtube.com/shorts/Lj7yCi2oDeo?si=GCSBrgnZZGK95ZWx "Everything Is AWESOME")
