# Emergency Accident Alert System

Traffic collisions around the world are a major cause of deaths, injuries, and property damage every year. Many deaths in accidents are caused by delays in getting the injured person to the hospital. Additionally, bystanders often hesitate to report accidents due to the fear of getting involved in the process. This project aims to reduce the probability of deaths after accidents by providing immediate notifications to nearby multi-specialist hospitals and police stations.

## Overview

The Emergency Accident Alert System detects accidents using an ADXL335 accelerometer sensor. When a significant impact is detected, the system calculates the magnitude of the impact. If the magnitude exceeds a certain threshold, the system tracks the location, sounds a buzzer for 10 seconds, and then sends a phone call and an SMS containing the location of the accident to a specified phone number. In case of a false alarm, a push button allows the user to stop the alert from being sent.

## Features

- **Impact Detection**: Uses the ADXL335 accelerometer sensor to detect sudden changes in vehicle axes due to a crash or accident.
- **Magnitude Calculation**: Calculates the magnitude of impact using a predefined algorithm.
- **Location Tracking**: Uses the NEO-6M GPS module to track the latitude and longitude of the accident location.
- **Alert Notification**: Sends a phone call and an SMS with the accident location to a specified phone number if the impact magnitude exceeds 50.
- **False Alarm Prevention**: Allows users to cancel the alert by pressing an embedded push button within 10 seconds.
- **Real-time Display**: Uses a 16×2 LCD display to show real-time status and impact information.

## Components

- **ADXL335 Accelerometer Sensor**: Detects impact and changes in vehicle axes.
- **NEO-6M GPS Module**: Tracks the geographical location of the accident.
- **SIM800L GSM Module**: Sends SMS notifications and makes phone calls.
- **Arduino Nano**: Microcontroller that processes the sensor data and controls the system.
- **16×2 LCD Display**: Displays real-time status and impact information.
- **Buzzer**: Alerts users with a sound for 10 seconds before sending the notification.
- **Push Button**: Allows users to cancel false alarms.

## How It Works

1. **Impact Detection**: The ADXL335 sensor detects a sudden change in the vehicle's axes.
2. **Magnitude Calculation**: The system calculates the magnitude of the impact. If it is less than 50, the system does not send an alert.
3. **Location Tracking**: If the magnitude is greater than 50, the system tracks the latitude and longitude using the GPS module.
4. **Alert Notification**: The system sounds a buzzer for 10 seconds. If the push button is not pressed within this time, the system sends a phone call and an SMS with the accident location to the specified phone number.
5. **False Alarm Prevention**: If the push button is pressed within 10 seconds, the alert is cancelled.

## Installation and Setup

1. **Hardware Setup**:
   - Connect the ADXL335 accelerometer sensor to the Arduino Nano.
   - Connect the NEO-6M GPS module to the Arduino Nano.
   - Connect the SIM800L GSM module to the Arduino Nano.
   - Connect the 16×2 LCD display to the Arduino Nano.
   - Connect the buzzer and push button to the Arduino Nano.

2. **Software Setup**:
   - Install the Arduino IDE from [Arduino's official website](https://www.arduino.cc/en/Main/Software).
   - Install the necessary libraries for the ADXL335, NEO-6M, and SIM800L modules.
   - Upload the provided code to the Arduino Nano using the Arduino IDE.

3. **Configuration**:
   - Set the specified phone number in the code to receive the alerts.
   - Adjust the impact magnitude threshold in the code if needed.

## Usage

1. Power on the system.
2. The system will monitor the vehicle's movements in real-time.
3. In case of a significant impact, the system will calculate the magnitude and, if necessary, start the alert process.
4. If no false alarm is detected, the system will send the accident location to the specified phone number.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- This project is inspired by the need to reduce fatalities in road accidents by providing timely alerts to emergency services.

