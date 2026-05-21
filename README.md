# IoT26-HW05

## Project Overview
This project demonstrates how to set up **Home Assistant on Raspberry Pi** and create a simple home automation environment.  
Using Home Assistant, Raspberry Pi can act as a smart home hub to monitor and control IoT devices through a web dashboard.

---

## Objective
- Install Home Assistant on Raspberry Pi
- Access the Home Assistant dashboard
- Learn the basics of home automation
- Practice Raspberry Pi based IoT integration

---

## Hardware Setup
- Raspberry Pi 5
- microSD Card
- Power Supply
- Wi-Fi / Ethernet Connection
- Laptop or PC for remote access

---

## Installation Process

### 1. Install Raspberry Pi Imager
Download and install Raspberry Pi Imager from the official website.

### 2. Flash Home Assistant OS
- Open Raspberry Pi Imager
- Select:
  - **Device:** Raspberry Pi 5
  - **Operating System:** Home Assistant OS
  - **Storage:** microSD Card
- Flash the image

### 3. Boot Raspberry Pi
Insert the microSD card into Raspberry Pi and power it on.

### 4. Access Home Assistant
Open browser and connect to:

```bash
http://homeassistant.local:8123
```

or

```bash
http://<RaspberryPi_IP_Address>:8123
```

### 5. Initial Setup
- Create administrator account
- Configure location and network
- Finish onboarding setup

---

## Home Assistant Dashboard
- Device monitoring
- Automation management
- Smart home integration
- Real-time IoT control

<img height="400" alt="image" src="https://github.com/user-attachments/assets/c3b9d281-7a88-4ba5-958f-3ef23925a99e" />


---

## Simple Automation Example

Example: Turn on a light automatically when motion is detected.

```yaml
automation:
  - alias: Motion Detected Light On
    trigger:
      platform: state
      entity_id: binary_sensor.motion_sensor
      to: "on"

    action:
      service: light.turn_on
      target:
        entity_id: light.room_light
```

---

## Reference
Tutorial followed:

- https://randomnerdtutorials.com/getting-started-with-home-assistant-on-raspberry-pi/

---

## Result
- Successfully installed Home Assistant on Raspberry Pi
- Accessed dashboard through browser
- Created basic home automation rule
<img height="400" alt="image" src="https://github.com/user-attachments/assets/c1826e6b-bccc-4e9d-ac22-301012a3a229" />


---

## Repository
- Notion
https://www.notion.so/Team-F-34f502a3cc6c80aa8522e0026b441b93

---
