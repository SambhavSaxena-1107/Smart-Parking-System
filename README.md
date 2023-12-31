**ABSTRACT:**

Smart car parking project aims at providing a confusion free and easy parking. This project helps the drivers of the cars to park their vehicles with minimum wastage of time with accurate information of the availability of the space to park It includes an Arduino Uno as the microcontroller unit to which the servo motors, LCD display ultrasonic sensors (HC-05) are interfaced. The LCD displays the availability of the space, the ultrasonic sensors keeps the check of the number of cars entering and exiting the parking space. The ultrasonic sensors detect the availability of the parking space.

**THEORY:**

An automated car parking system is a process through which car parking can be done more efficiently and easily than manual method. The system will provide the user better services. The system counts the number of cars in the garage and checks if there’s any vacancy. There’s an entry and exit path. When vehicle enters, the display shows the number of cars inside. When any vehicle leaves, the count decreases and shown on display. If the garage is full. The display will show a message regarding that. This whole process includes the use of Arduino, Display and sonar. The sonar detects whether the vehicle is entering or leaving. The report then showed on display.

![image](https://github.com/SambhavSaxena-1107/Smart-Parking-System/assets/126766980/d645ab3d-cc61-4cde-bfe9-cfe07afe2722)

**Hardware Components:**

Arduino UNO,
Ultrasonic Sensor,
LCD Screen,
Bread Board,
Power Supply,
Connecting Wires.

![image](https://github.com/SambhavSaxena-1107/Smart-Parking-System/assets/126766980/baf76884-f34d-47f1-b14c-7085fc7d6571)

**System Testing:**

We have tested the design system with a dummy car. There are usually two possibilities. • Entry : While entering, the car is noticed by the sonars. Firstly the outer sonar and then the inner sonar. The count increases and result is shown in display. • Exit : In this case, Firstly the inner sonar notices and then the inner sonar. The count decreases and result is shown in display.


**Experimental Results:**

We have experimented the system to gather some statistical results. After the experience, we have found the inner sonar and outer sonar works perfectly. As the result shows, the system is almost 100% correct. The whole experiment was done couple of times by us. Dummy cars were used. The prototype was not always correct due to the limitations of the use of low quality sensors. But the performance was satisfactory enough.

**References:**

https://www.engineersgarage.com/electronic-components/16x2-lcd-module-datasheet

https://store.arduino.cc/usa/arduino-uno-rev3

http://www.micropik.com/PDF/HCSR04.pdf
