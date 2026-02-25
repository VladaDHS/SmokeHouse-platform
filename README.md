# SmokeHouse-platform
# Smart Smokehouse

An IoT-based automated smokehouse system built on ESP32, ESPHome and Home Assistant.

This project provides a complete solution for building a smart smokehouse including:
- Temperature control
- Smoke generation control
- Meat temperature monitoring
- Heating element regulation
- Hardware wiring documentation
- Home Assistant integration

The goal is to create a stable, automated smokehouse control system with full remote monitoring and automation capabilities. 
To ensure stable enviromet with minimum user intereference for precice meat smoking. 


---

## Project Overview

Smart Smokehouse is designed as a modular system consisting of:

- Smokehouse chamber
- Control cabinet (controller unit)
- Smoke generator
- Sensors and measurement
- Firmware (ESPHome)
- Home Assistant integration
- Hardware documentation

The system is designed for DIY builders who want professional-level control over their smoking process.
You can build your own Smokehouse from scratch or just use modules to upgrade you curent solution. 

---

## 1. Smokehouse Chamber

The smokehouse chamber is the insulated enclosure where the smoking process takes place.

Features:
- Internal air temperature monitoring (DS18B20)
- Multiple meat probes (MAX31865 PT100/PT1000)
- Controlled heating element
- Air circulation fan -TBD
- Controlled smoke generator

The chamber is designed to maintain stable temperature and smoke delivery.

---

## 2. BRAIN - Control unit

Brain of whole system is based on ESP32. Complex eletrical box containtig all nessesary component to mesure and controle. 
LCD for control of temperature and times. Actual smoking status - Temperature, time, heating status.  


Main components:
- ESP32 microcontroller
- Solid state relays (SSR)
- Power relays
- Power supply unit
- Protection elements (fuses, breakers)
- LCD 2004 display
- Rotary encoder with push button

Responsibilities:
- Heating element control
- Smoke generator control
- Safety monitoring
- User interface handling
- Communication with Home Assistant

The cabinet separates low-voltage logic from high-voltage power circuits for safety.

---

## 3. Smoke Generator

The smoke generator is a robust smoke generator for cold smoking that produces a steady flow of clean smoke.
It burns smoking chips in a small combustion chamber, and the resulting smoke is actively extracted by a ventilation unit and pushed into the smoker. 
Its design also removes tar from the smoke, ensuring only clean, cool smoke enters the smoking chamber.
This solution alow also long cold smoking. 

Possible implementation:
- External smoke box
- Wood chip or pellet based system
- Air pump or fan assisted combustion

Control options:
- On/off control
- Timed smoke cycles
- Temperature-dependent smoke control
- Manual override via UI or Home Assistant

---

## 4. Sensors & Monitoring

### Chamber Temperature
- DS18B20 digital temperature sensor

### Meat Temperature
- MAX31865 with PT100/PT1000 probes
- Multiple independent channels

### Optional
- Humidity sensor
- Ambient temperature sensor
- Current monitoring (energy usage)

All data is exposed to Home Assistant via ESPHome.

---

## 5. Firmware (ESPHome)

The system firmware is built using ESPHome.

Features:
- PID temperature control
- Automation logic
- OTA updates
- Native Home Assistant integration
- Local manual control
- Fail-safe behavior

Configuration files are stored in the `firmware/` directory.

---

## 6. Home Assistant Integration

The smokehouse integrates directly with Home Assistant.

Capabilities:
- Real-time monitoring
- Temperature graphs
- Automation triggers
- Notifications
- Remote control
- Logging of smoking sessions

Example use cases:
- Notify when meat reaches target temperature
- Automatically stop heating
- Trigger cooldown phase
- Start smoke cycle based on schedule

---

## 7. Safety

Safety is a critical aspect of this project.

Implemented measures:
- Thermal limits
- Watchdog restart
- Relay fail-safe state
- Power separation
- Manual emergency shutdown

⚠️ High voltage components must be installed by a qualified person.

---

## 8. Project Structure

---

## 9. Future Improvements

- Automatic humidity regulation
- Full PID auto-tuning
- Session logging & export
- Web interface
- Multi-chamber support
- Cloud dashboard

---

## License

This project is open-source and intended for DIY and educational purposes.
Use at your own risk.
