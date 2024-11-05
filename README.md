# Dog-Activity-Tracker-project-using-ESP32

A project that monitors a dog's activity using an ESP32 microcontroller, a simulated accelerometer/gyroscope, and LittleFS for data storage. The tracker categorizes activities (Resting, Walking, Running, and Playing) and stores the data for easy syncing with a mobile app.

## Project Overview

The Dog Activity Tracker uses:
- **Simulated Accelerometer**: Emulates a QMI8658 sensor to provide motion data.
- **Activity Classification**: Simple thresholds to classify activities.
- **Data Storage**: LittleFS stores activity data in 10-minute intervals.
- **Time Management**: ESP32 RTC manages time with NTP syncing when Wi-Fi is available.

## Requirements

**Hardware**:
- ESP32-S3 microcontroller

**Libraries**:
- ESP32 Arduino Core (v2.0.14)
- LittleFS
- BLE and ArduinoOTA (for optional extensions)

## Setup

1. **Clone Repository**: Clone or download this repo.
2. **PlatformIO Setup**: Configure and install dependencies via `platformio.ini`.
3. **Upload Code**: Flash code to your ESP32 with `pio run --target upload`.
4. **Monitor Activity**: Use the serial monitor to view activity classifications.

## Modules

- **SimulatedQMI8658**: Provides dummy accelerometer and gyro data.
- **ActivityClassifier**: Classifies activities based on thresholds.
- **DataStorage**: Saves activity data on LittleFS.
- **TimeManager**: Manages time and syncs with NTP.

## Future Improvements

Planned features include advanced classification with TensorFlow Lite, BLE data sync, and real sensor integration.

---

This project is open-source under the MIT License. 
