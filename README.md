# IOT-based-low-cost-ECG-and-heart-monitoring-System
AIM: To provide accessible and continuous remote monitoring of a person’s cardiac health.

INTRODUCTION:

IoT-based low-cost ECG monitoring system offers a transformative solution for democratizing access to cardiac care. By leveraging the power of the Internet of Things, this system provides continuous and affordable monitoring of the heart's electrical activity.

OBJECTIVE:

*Early Detection of Cardiac Issues

*Remote Patient Monitoring

*Low-Resource Settings

*Reducing Healthcare Costs

*Education and Research

FEATURES:

*Develop a Wearable Heart Monitoring Device:

Design a compact and wearable device capable of continuous ECG monitoring using the ESP32 and AD8232.

*Real-Time ECG Signal Processing:

Implement real-time signal processing algorithms to filter noise and extract meaningful ECG data for accurate heart rate calculation.

*Wireless Data Transmission:

Enable wireless data transmission from the monitoring device to a connected device (e.g., smartphone, computer) for real-time display and analysis.

*Heart Rate Calculation Algorithm:

Develop and optimize algorithms to calculate the user's heart rate based on the processed ECG signals.

*User Alerts for Abnormalities:

Implement an alert system to notify users in real-time of irregular heartbeats or abnormal ECG patterns, promoting early detection of potential health issues.

*Data Logging and Storage:

Create a data logging feature to store ECG data over time, facilitating historical analysis and tracking of changes.

*Cloud Integration:

Integrate cloud storage for ECG data, allowing users to access their information from multiple devices and enabling remote monitoring by healthcare professionals.

*Bluetooth Connectivity:

Develop power-saving features to optimize battery life, including sleep modes and low-power states, particularly for wearable applications.

*User Authentication and Privacy:

Implement user authentication mechanisms to ensure secure access to ECG data and prioritize user privacy in compliance with relevant regulations.

*Intuitive User Interface:

Design an intuitive and user-friendly interface for displaying real-time ECG data, heart rate, and historical trends.

*Customizable Settings:

Provide users with customizable settings, such as monitoring duration, alert thresholds, and display preferences, to enhance the user experience.

*Integration with Health Platforms:

Explore integration with existing health platforms or applications, allowing users to sync ECG data with other health-related metrics for a comprehensive health profile.

*Offline Mode and Local Data Storage:

Include an offline mode that stores a certain amount of data locally, enabling users to access their ECG history even without an internet connection.

*Open-Source Collaboration:

Foster open-source collaboration by making the project's codebase accessible to the developer community, encouraging contributions and improvements.

*Educational Resources:

Provide educational resources within the application to help users understand their ECG data, promoting heart health awareness and informed decision-making

COMPONENTS REQUIRED:

*ESP32 Board

*AD8232 ECG sensor

*ECG Electrode connector with plastic patches

*Connecting wires

MINDMAP:

![Screenshot 2023-11-20 100327](https://github.com/sushmakarkera/IOT-based-low-cost-ECG-and-heart-monitoring-System/assets/149661660/097f95bf-60cc-4d30-b25d-46db1b7482cf)

Working:

ECG Sensors: The system begins with the use of ECG sensors or electrodes placed on the patient's body to measure the electrical activity of the heart. These sensors detect the small electrical signals generated by the heart during each heartbeat.
Signal Acquistion: The ECG sensors capture the analog signals, which represent the heart's electrical activity. These signals are then converted into digital data for further processing.
Microcontroller or Processing Unit: A microcontroller or a processing unit is used to process the digital ECG signals. This unit may filter, amplify, and digitize the signals to prepare them for transmission.
Wireless Communication: An integral part of an IoT-based system is wireless communication. The processed ECG data is transmitted using wireless protocols such as Wi-Fi

FLOWCHART:

![flowchart](https://github.com/sushmakarkera/IOT-based-low-cost-ECG-and-heart-monitoring-System/assets/149661660/37d5d1ce-e78b-48d7-91ae-169d3befa4c4)

Algorithm:

STEP1: Include Libraries
•	Include necessary libraries such as ‘WiFi.h’, ‘WiFiUdp.h’, ‘PubSubClient.h’ and ‘NTPClient.h’.

STEP 2: Define constants
•	Define constants for WIFI credentials, variable labels, device label and sensor pin.

STEP 3: Global variables
•	Declare global variable for MQTT broker, payload, topic and various time-related variables.

STEP 4: Main functions
•	Implement the ‘setup()’ function
•	Connect to WiFi 
•	Set sensor pin as INPUT
•	Implement the ‘loop()’ function
•	Check if MQTT client is connected; if not, attempt to reconnect
•	Increment a counter variable ‘j’
•	Construct MQTT topic using device label
•	Publish the payload

STEP 5: Data formatting
•	Format sensor reading and time stamp as strings
•	Utilize ‘printf’ to construct the MQTT payload 

STEP 6: Publish Data
•	Publish the constructed payload

STEP 7: Delay
•	Introduce the delay of 150 millisecond between sensor reading

STEP 8: Serial Output
•	Output relevant information to the serial monitor for debugging and monitoring.

Block Diagram:

![image](https://github.com/sushmakarkera/IOT-based-low-cost-ECG-and-heart-monitoring-System/assets/149661660/56b16e59-03c0-4550-9664-14fd3fe5ad3a)

Circuit Diagram:

![circuit](https://github.com/sushmakarkera/IOT-based-low-cost-ECG-and-heart-monitoring-System/assets/149661660/1f2c64eb-9405-40e2-9319-aeeb3fe88735)




