# ♻️ Reverse Vending Machine

A smart Reverse Vending Machine developed using **Raspberry Pi 4**, **Arduino Mega**, and **ESP8266** to automatically identify recyclable waste, sort it, reward users for plastic bottle recycling, and notify the operator when the machine is full using IoT.

---

# 📖 Project Overview

The Reverse Vending Machine is an intelligent recycling system designed to encourage proper waste disposal. It automatically identifies whether the inserted object is a **plastic bottle** or a **metal can** using image processing, sorts the waste into separate compartments, rewards users for recycling plastic bottles, and sends a notification to the operator when the collection bin becomes full.

The project was developed primarily using recycled electronic components and scrap materials to demonstrate a sustainable and low-cost engineering solution.

---

# 🎯 Objective

The objective of this project is to develop an automated recycling system capable of:

- Identifying recyclable waste using image processing.
- Automatically sorting plastic bottles and metal cans.
- Providing rewards for plastic bottle recycling.
- Monitoring waste-bin capacity using IoT.
- Promoting sustainable waste management.

---

# 🎯 Project Aim

- Build an intelligent recycling machine using Embedded Systems.
- Integrate Raspberry Pi, Arduino Mega, and ESP8266 into a single system.
- Implement real-time image processing.
- Automate waste segregation.
- Demonstrate IoT-based monitoring.
- Encourage recycling through an automated reward system.

---

# ⚙️ System Workflow

## 1. User Detection

The front side of the machine is equipped with an **Ultrasonic Sensor** that continuously detects whether a user is approaching the machine.

When a user comes near the machine:

- The ultrasonic sensor detects the presence of the user.
- Arduino Mega activates the front servo motor.
- The front door automatically opens.
- After the user inserts the recyclable item, the door closes automatically.

---

## 2. Object Placement

The inserted object enters the first inspection chamber where it is temporarily stopped.

This chamber contains:

- Camera Module
- Object holding mechanism

The object remains stationary until image processing is completed.

---

## 3. Image Processing

The Raspberry Pi captures an image using the camera module.

Using OpenCV-based image processing, the Raspberry Pi identifies whether the object is:

- Plastic Bottle
- Metal Can

After classification, Raspberry Pi sends a digital output signal to the Arduino Mega.

---

## 4. Plastic Bottle Sorting

If the detected object is a **Plastic Bottle**:

- Raspberry Pi sets Digital Output Pin 1 HIGH.
- Arduino Mega receives the signal.
- The internal servo mechanism opens the plastic bottle pathway.
- The bottle is transferred into the plastic collection compartment.

After successful disposal:

- Arduino activates the reward mechanism.
- A dedicated servo motor rotates to release a reward coin.
- The user receives the reward automatically.

---

## 5. Metal Can Sorting

If the detected object is a **Metal Can**:

- Raspberry Pi sets Digital Output Pin 2 HIGH.
- Arduino Mega receives the signal.
- The metal can pathway is opened.
- The can is transferred into the metal collection compartment.

No reward is provided for metal cans.

---

## 6. Bin Level Monitoring

Inside the waste collection compartment, an **ESP8266** continuously monitors the fill level using an **Ultrasonic Sensor**.

The sensor measures the remaining storage space.

When the collection bin reaches the predefined level:

- ESP8266 detects that the machine is nearly full.
- The data is transmitted over Wi-Fi.
- Notification is sent to the machine operator using **Blynk IoT**.

This allows timely waste collection and prevents overflow.

---

# 🛠 Hardware Used

| Hardware | Purpose |
|----------|----------|
| Raspberry Pi 4 | Image Processing & Decision Making |
| Arduino Mega | Hardware Control & Servo Management |
| ESP8266 | IoT Communication |
| Camera Module | Object Image Capture |
| Ultrasonic Sensor | User Detection |
| Ultrasonic Sensor | Bin Level Monitoring |
| Servo Motors | Door Control, Sorting Mechanism & Reward System |
| DC Motor (CD Drive Motor) | Internal Mechanical Movement |

---

# 💻 Software Used

- Python
- OpenCV
- Arduino IDE
- Embedded C/C++
- Raspberry Pi OS
- Blynk IoT Platform

---

# ⭐ Key Features

- Automatic user detection
- Automatic entrance door
- Image processing-based waste identification
- Plastic bottle recognition
- Metal can recognition
- Automatic waste segregation
- Coin reward mechanism
- Servo-based sorting system
- IoT-based fill level monitoring
- Remote notification through Blynk
- Sustainable design using recycled components

---

# 📚 Skills & Experience Gained

During this project, I gained practical experience in:

- Raspberry Pi Development
- Arduino Mega Programming
- ESP8266 IoT Development
- Python Programming
- OpenCV Image Processing
- Embedded System Design
- Sensor Integration
- Servo Motor Control
- Multi-controller Communication
- Hardware Debugging
- Mechanical System Design
- Real-time Decision Making
- IoT Cloud Integration
- Blynk Platform
- System Testing & Troubleshooting

---

# 🚧 Challenges Faced

- Synchronizing Raspberry Pi and Arduino Mega.
- Reliable image detection under different lighting conditions.
- Designing the bottle stopping mechanism.
- Mechanical alignment of sorting pathways.
- Developing the automatic reward mechanism.
- Integrating IoT monitoring with the waste collection compartment.
- Building the prototype using recycled electronic components.
- Testing and debugging hardware and software simultaneously.

---
# Project Photos 
![Image1 ](https://github.com/Sulfikarpk/Reverse_vending-_machine/blob/main/RVM%20image1.jpeg)

---
![Image2](https://github.com/Sulfikarpk/Reverse_vending-_machine/blob/main/RVM_image_2.jpeg)

---

# 🎥 Project Demonstration

-part1 testing (https://youtube.com/shorts/mPhIaO_0eBw)
---
-part2 testing (https://youtube.com/shorts/nCFgtVitJv4)
---
-part3 final testing ()
---

---

# 🔮 Future Improvements

- AI-based object recognition using TensorFlow Lite
- Automatic bottle crushing mechanism
- QR Code reward system
- Mobile application
- Cloud database integration
- LCD user interface
- Online dashboard for multiple machines
