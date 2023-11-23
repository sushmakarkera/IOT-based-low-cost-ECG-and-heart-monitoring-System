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

ECG Sensor: Connect an ECG sensor to the ESP32 to capture electrical signals from the heart.

Signal Processing: Use the ESP32 to process the raw ECG signals. You may need to filter, amplify, and digitize the signals for further analysis.

Voltage analysis: Analyze the processed signals to calculate and compare the voltage values.

Display on LCD: Use the ESP32 to send the heart rate information to the LCD for real-time display. The LCD can show whether the heart condition is good or bad based on predefined thresholds or algorithms.

User Interface: Implement user interaction via buttons or a touchscreen if needed. Users may want to start/stop monitoring or view historical data.

Communication: Optionally, you can add features to send data to a remote server or a mobile app for more comphrensive monitoring.

FLOWCHART:

![flowchart](https://github.com/sushmakarkera/IOT-based-low-cost-ECG-and-heart-monitoring-System/assets/149661660/37d5d1ce-e78b-48d7-91ae-169d3befa4c4)

Algorithm:

STEP1:Initialization

Include Libraries: Include the LiquidCrystal, WiFi, and ThingSpeak libraries.

STEP2:Create Objects

Create a LiquidCrystal object for the LCD.

Declare variables for WiFi credentials, ThingSpeak channel information, and a WiFi client.

STEP3:Setup Function:

Serial and LCD Initialization:

Begin serial communication at a baud rate of 9600.

Initialize the LCD with its specific pins.

STEP4:Leads Off Detection Setup:

Set pin 15 as INPUT for leads off detection (LO +).

Set pin 21 as INPUT for leads off detection (LO -).

STEP5:WiFi Connection:

Connect to the WiFi network using the provided SSID and password.

ThingSpeak Initialization:

Initialize ThingSpeak communication using the ThingSpeak library and the WiFi client.

STEP6:Loop Function:

Analog Sensor Reading:

Read the analog value from pin A0 using analogRead().

STEP7:LCD Display:

Clear the LCD display.

Check for leads off condition:

If leads off is detected (digitalRead on pins 15 or 21 is 1), handle the condition as needed.

If leads are on:

Display "Analog: " and the analog value on the LCD.

Display "Health: Good" if the analog value is between 500 and 3000; otherwise, display "Health: Bad."

STEP8:Serial Output:

Print the analog value to the Serial Monitor.

ThingSpeak Data Sending:

Set ThingSpeak fields with the analog value and timestamp.

Send the data to ThingSpeak using ThingSpeak.writeFields().

STEP9:Success/Failure Message:

If the response code from ThingSpeak is 200, print "Data sent to ThingSpeak successfully" to the Serial Monitor.

If the response code is not 200, print "Failed to send data to ThingSpeak" to the Serial Monitor.

STEP10:Delay:

Introduce a delay of 1000 milliseconds to prevent saturation of LCD and Serial data.

STEP11:Repeat:

Loop back to step 7 and repeat the process.


Block Diagram:

![image](https://github.com/sushmakarkera/IOT-based-low-cost-ECG-and-heart-monitoring-System/assets/149661660/56b16e59-03c0-4550-9664-14fd3fe5ad3a)

Circuit Diagram:

![circuit](https://github.com/sushmakarkera/IOT-based-low-cost-ECG-and-heart-monitoring-System/assets/149661660/1f2c64eb-9405-40e2-9319-aeeb3fe88735)




