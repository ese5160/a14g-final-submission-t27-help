[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/kzkUPShx)
# a14g-final-submission

    * Team Number: 27
    * Team Name: HELP
    * Team Members: Yuxin Qian & Yuxuan Chen
    * Github Repository URL: https://github.com/ese5160/a14g-final-submission-t27-help/edit/main/README.md
    * Description of test hardware: (development boards, sensors, actuators, laptop + OS, etc) laptop

## 1. Video Presentation   
>Please click [here](https://youtu.be/XZ_qUomz5_s) to watch our video presentation.
> 
## 2. Project Summary   
- **Device Description**
>Our device Vibrapath Waist Pack is designed to assist individuals with visual impairments. It features a wearable belt that alerts the user through vibrations from built-in motors, which are activated based on the proximity of obstacles detected in front. Additionally, the device incorporates fall detection functionality utilizing real-time data from an integrated IMU.     
       
>This is an IoT-enabled device that connects via Wi-Fi to a user interface (UI). The UI displays real-time sensor data, provides alert functionalities, and includes buttons for remotely updating the device firmware. This connectivity enhances user experience by ensuring they can monitor the device's status and receive critical updates effortlessly.      
     
- **Inspiration**    
>The development of the Vibrapath waist pack was motivated by the challenges faced by the visually impaired community in navigating their environments safely and independently. The stark reality that many visually impaired individuals encounter daily hazards and obstacles that could be mitigated with the right technology sparked our commitment to this project.  
   
>Our goal was to harness sensor technologies and IoT connectivity to create a practical, wearable device that could make a significant difference. By integrating an IMU and a distance sensor, the waist pack provides immediate tactile feedback through vibrations, warning users of nearby obstacles and changes in the terrain. This feature allows for safer and more confident mobility, giving users the ability to perceive their surroundings in a nuanced way.   
  
>We chose to design this product because we recognized a profound need for innovative solutions that could extend the sensory world to those with visual impairments, enhancing their freedom and quality of life.   
     
- **Device Functionality**    
>Our device integrates key components to assist visually impaired individuals. It utilizes an IMU and a distance sensor, enabling two main functions:    
>>**1. Obstacle Detection:** The distance sensor gauges the distance to nearby objects, triggering vibrations through a motor if an obstacle is too close, alerting the user via tactile feedback.      
>>**2. Fall Detection:** The IMU monitors acceleration to detect falls, issuing alerts through the UI if abnormal movements are detected.
    
>**Connectivity:**   
Features Wi-Fi connectivity, linking the device to a Node-RED UI via the MQTT protocol for seamless data transmission and remote firmware updates.    

>**Block Diagram:**              
> <img width="600" alt="image" src="https://github.com/ese5160/a14g-final-submission-t27-help/blob/main/image/block.png">        
     
- **Challenges**
>Throughout our project, we encountered a variety of unexpected issues, each providing a learning opportunity and enhancing our problem-solving skills.     
    
>1. **Sensor Sensitivity:**    
>>**Problem:** Our distance sensor was overly sensitive, often erroneously displaying a distance of zero during tests.      
>>**Solution:** After multiple checks of the wiring, we discovered and removed a dust particle from the sensor's ultrasonic probe, which restored accurate readings.       
     
>2. **Memory Limitations:**    
>>**Problem:** We frequently faced issues with insufficient memory, causing the software to freeze and the serial output to halt.     
>>**Solution:** We addressed this by continuously adjusting the size and priority of each task in our program.    
         
>**Reflection:**    
>These challenges highlighted the discrepancies between theory and practical implementation. Our hands-on resolution of these issues not only fixed immediate problems but also equipped us with invaluable practical insights that theoretical learning could not have provided.
       
- **Prototype Learnings**
>Throughout the process of building and testing our prototype, we recognized the critical importance of thoughtful component placement and the strategic use of jumpers for circuit protection during tests. These insights have underscored the need for careful design considerations in future projects. Should we design and build another PCB, we plan to incorporate jumpers at key voltage output locations to safeguard the circuit and will conduct a thorough review of layout rules to enhance overall wiring efficiency and safety.         
  
- **Next Step**
>Given more time, we aim to enhance the firmware to enable adaptive vibration feedback based on varying distances to obstacles. This upgrade would involve programming the haptic driver to operate in different modes, providing users with distinct levels of vibration feedback depending on the proximity of the detected obstacles. This improvement will make the device more intuitive and responsive, greatly enhancing user experience.
        
- **Takeaways from ESE5160**
>**Electronics and Circuit Design:** Developed a deeper understanding through hands-on designing and prototyping of complex systems.    
>**Microcontroller Programming:** Gained practical experience in programming and integrating sensors and actuators into cohesive systems.  
>**Project Management and Teamwork:** Learned the importance of effective project management and communication within teams.  
>**Testing and Troubleshooting:** Acquired best practices for testing and troubleshooting complex electronic systems.  
>**User Interface and Communication Protocols:** Gained experience in creating and hosting user interfaces with Node-RED and utilizing MQTT protocols for embedded systems communication.
   
- **Project Links**
> Our firmware code can be accessed by clicking [here](https://github.com/ese5160/a12g-firmware-drivers-t27-help/blob/main/HELP_fireware_code_final.7z).
> Our nodered code can be accessed by clicking [here](https://github.com/ese5160/a14g-final-submission-t27-help/blob/d8b815f46642ff05eff49a00cadfbac6f77b3d2b/.vscode/nodered.json)
## 3. Hardware & Software Requirements
Hardware requirements:

Our project is a wearable electronic device based on SAMW25 as a microcontroller designed to assist blind individuals by detecting potential obstacles and alerting them via haptic feedback. The device uses an ultrasonic distance sensor to detect potential obstacles, combined with a three-axis accelerometer to detect falls. In an emergency, it automatically communicates with the blind person's family via Wi-Fi.
The hardwares we used are: ultrasonic distance sensor, 3-axis acceleration sensor, haptic motor driver and motor. The differences between the very early of this semester and our output are:
First, we change a different kind of distance sensor. We change from HC-SR04 to US-100 because the reference code we found online were always US-100 and it was easier to modify from the US-100 code.
Seconde, we change from 3-axis accelerometer to IMU. They have the same function but only the first one uses SPI communication protocol while the other use I2C. And we failed to write SPI code ourselves so we choose I2C and it is easier to write.

Software requirements:

At its core, the software integrates with the SAMW25 module to manage sensory input from the imu and an ultrasonic sensor, interpreting this data to provide instantaneous haptic feedback and fall detection. The software enables the device to act as an intelligent intermediary between the user and their environment, translating complex sensory information into simple, actionable alerts.
We completed all the software tasks and made a nodered UI.

## 4. Project Photos & Screenshots
>final project:

> <img width="600" alt="image" src="https://github.com/ese5160/a14g-final-submission-t27-help/blob/main/image/shell1.jpg">
><img width="600" alt="image" src="https://github.com/ese5160/a14g-final-submission-t27-help/blob/main/image/shell2.jpg">

>top view of standalone PCBA:

><img width="600" alt="image" src="https://github.com/ese5160/a14g-final-submission-t27-help/blob/main/image/pcb_top.jpg">

>bottom view of standalone PCBA:

><img width="600" alt="image" src="https://github.com/ese5160/a14g-final-submission-t27-help/blob/main/image/pcb_bottom.jpg">

>thermal image of PCBA:

><img width="600" alt="image" src="https://github.com/ese5160/a14g-final-submission-t27-help/blob/main/image/thermal.png">

>2D view of Altium Board design:

><img width="600" alt="image" src="https://github.com/ese5160/a14g-final-submission-t27-help/blob/main/image/PCB.png">

>3D view of Altuim Board design:

><img width="600" alt="image" src="https://github.com/ese5160/a14g-final-submission-t27-help/blob/main/image/3D.png">

>NODE-RED dashboard:

><img width="600" alt="image" src="https://github.com/ese5160/a14g-final-submission-t27-help/blob/main/image/nodered_ui.png">
><img width="600" alt="image" src="https://github.com/ese5160/a14g-final-submission-t27-help/blob/main/image/NODERED_UI2.png">
><img width="600" alt="image" src="https://github.com/ese5160/a14g-final-submission-t27-help/blob/main/image/NODERED_UI3.png">

>NODE-RED backend:

><img width="600" alt="image" src="https://github.com/ese5160/a14g-final-submission-t27-help/blob/main/image/NODERED_1.png">
><img width="600" alt="image" src="https://github.com/ese5160/a14g-final-submission-t27-help/blob/main/image/NODERED_2.png">
><img width="600" alt="image" src="https://github.com/ese5160/a14g-final-submission-t27-help/blob/main/image/NODERED_3.png">

>block diagram:

> <img width="600" alt="image" src="https://github.com/ese5160/a14g-final-submission-t27-help/blob/main/image/block.png">   

## 5. A12G Codebase   
> Our final embedded C firmware codebases can be accessed by clicking [here](https://github.com/ese5160/a12g-firmware-drivers-t27-help/blob/main/HELP_fireware_code_final.7z).
> 
