[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/kzkUPShx)
# a14g-final-submission

    * Team Number: 27
    * Team Name: HELP
    * Team Members: Yuxin Qian & Yuxuan Chen
    * Github Repository URL: https://github.com/ese5160/a14g-final-submission-t27-help/edit/main/README.md
    * Description of test hardware: (development boards, sensors, actuators, laptop + OS, etc) laptop

## 1. Video Presentation

## 2. Project Summary   
- **Device Description**
>Our device is designed to assist individuals with visual impairments. It features a wearable belt that alerts the user through vibrations from built-in motors, which are activated based on the proximity of obstacles detected in front. Additionally, the device incorporates fall detection functionality utilizing real-time data from an integrated IMU.     
       
>This is an IoT-enabled device that connects via Wi-Fi to a user interface (UI). The UI displays real-time sensor data, provides alert functionalities, and includes buttons for remotely updating the device firmware. This connectivity enhances user experience by ensuring they can monitor the device's status and receive critical updates effortlessly.      
     
- **Inspiration**    
>Our project was inspired by a systematic study of how to design a complete IoT embedded product. Through this process, we gained hands-on experience from component selection and schematic design to PCB layout and the development of firmware and Node-RED code. We found this comprehensive learning experience to be incredibly enriching, and believe it has equipped us with valuable skills that will significantly benefit our future work.
    
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
>Through the development and testing of our prototype, we gained valuable insights into the importance of component placement and protective measures in circuit design:    
        
>**Component Placement and Protection:**           
>>**Lesson:** The strategic placement of components and the inclusion of jumpers are crucial for both the functionality and safety of the circuit during testing.        
>>**Future Implementation:** In future PCB designs, we will prioritize the insertion of jumpers at voltage output points to protect the circuit and meticulously review our layout rules to optimize wiring configurations.
  
- **Next Step**
- **Takeaways from ESE5160**
- **Project Links**  
## 3. Hardware & Software Requirements

## 4. Project Photos & Screenshots
