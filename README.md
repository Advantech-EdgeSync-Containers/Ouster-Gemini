# Ouster-Gemini

Ouster Gemini is a lidar detection platform that combines Ouster 3D digital lidar sensors and AI-powered perception software. The system delivers precise, long-range detection, classification and tracking of people and vehicles and provides advanced situational awareness to enhance physical security, safety and operational efficiencies of critical infrastructure, and urban and business spaces. Built for extreme environments, Ouster Gemini helps to provide reliable detection in adverse weather or low light, while significantly reducing nuisance alarms indoors and outdoors.

**Ouster-Gemini** is a containerized AI LiDAR perception solution released by **Ouster, Inc.**. It is optimized for deployment on Advantech GPU-accelerated platforms such as **TREK-50N** and **TREK-60N**, and leverages Ouster's Gemini software for real-time object detection and scene understanding.

Ouster Gemini supports multi-sensor meshing into a single scene, low-latency detections, and can be integrated via REST APIs, WebSockets, or MQTTs streams. 

### *Ouster Gemini System Architecture*

![Ouster Gemini Overview](https://static.ouster.dev/ouster-detect/_images/gemini_intro.png)

It processes raw lidar pointcloud data from Ouster OS sensors and outputs structured, actionable information like: 
- 3D position and movement of people, different types of vehicles, and cyclists 
- Customers can configure #8 different rule engines aka Events, to add high level business logic alerting the customers of unwanted behaviors

### *Ouster Gemini OutdoorDetect Demonstrations*


![Ouster Gemini Outdoor Detect Demo](/doc/ouster-gemini-outdoordetect-demo.gif)

![Ouster Gemini Outdoor Detec Demo1](/doc/ouster-gemini-outdoordetect-1.gif)

### *Ouster Gemini people tracking demonstration*
![People detect](/doc/people-gemini.png)


![Gemini Preception page](/doc/gemini-preception-page.png)


### **Solution components:**
- Ouster 3D digital lidar sensors 
- Ouster Gemini AI-powered perception software
- Optional mounting, cable, and power accessories 
- Edge computer 
- Optional VMS integration


## Features

- AI-powered detection, classification and tracking at (up to) 90 meters/300ft (people, vehicles, bikes)
- Continuous tracking of objects and consistent ID with 2D & 3D digital twin visualization
- No-code advanced rule-engine events and alerts 
- Lidar 3D site coverage design tool
- Cloud portal interface to configure, manage, and view multiple deployments and events 
- VMS integration


![](https://ouster.imgix.net/02-Products/02-Software/Software-Gemini/06b-Ouster-software-gemini-step2-poster.png)

## Supported Hardware

- Ouster Rev6/Rev7 LiDAR sensors (OS0, OS1, OS2, OSDome)
- Advantech TREK-50N / TREK-60N (NVIDIA GPU-equipped)
- Compatible with Ouster Catalyst edge devices or custom edge computers


## System Requirements

- Ubuntu 20.04 or later (Linux)
- Docker (20.10+)
- NVIDIA Container Toolkit
- GPU recommended for Deep Learning workloads


## Installing Ouster Gemini

There are two ways to install **Ouster Gemini** for the first time:

1. **Using `get-detect.sh` script** – *Internet access required*
2. **Using a compressed archive (.tar.gz)** – *Internet access NOT required*. 
    - You must first download the archive from the [Ouster Artifact Repository](https://static.ouster.dev/ouster-detect/software_access/software_access.html#artifact-repository).

### Installation

1. **Access Gemini Software**
   - Request credentials from your Ouster representative.
   - Software is hosted on the [Ouster Artifact Repository](https://static.ouster.dev/ouster-detect/software_access/software_access.html#artifact-repository).

2. **Install and Launch**
   ```bash
   curl -O https://static.ouster.dev/ouster-detect/get-detect.sh
   chmod +x get-detect.sh
   ./get-detect.sh --vella
   ```

3. **Configuration**
   - Use provided UI or YAML files to configure zones and detection behavior.


## Getting Started to Access Gemini

To begin using Ouster Gemini, you must activate your license with a valid **Entitlement ID**. This can be done either **online via the GUI** or **offline via a license file**.

Steps include:
1. Launching Gemini and accessing the browser UI
2. Entering or uploading your license details in the UI

> **Note:** You can still access the Gemini UI without a license, but **you will not be able to connect to Ouster sensors** until activation is complete.

Full guide: [Getting Started with Ouster Gemini](https://static.ouster.dev/ouster-detect/getting_started/getting-started.html)


## Output Interfaces

- REST API (for configuration)
- TCP streaming (`object_list`, `occupations`, `clusters`, `diagnostics`)
- MQTT-based output supported


## Example Use Cases

- Crowd and retail analytics
- Security and intrusion monitoring
- Intelligent Transportation Systems (ITS)
- Full Yard tracking 
- Zone-Based-Alarms
- Position & Speed Tracking
- Object Classification


## References

- [Ouster Gemini Product Page](https://ouster.com/products/software/gemini)
- [Introduction to Gemini](https://static.ouster.dev/ouster-detect/introduction.html)
- [Hardware Integration](https://static.ouster.dev/ouster-detect/using_3rd_party_hardware/using-3rd-party-hardware.html)
- [Software Access](https://static.ouster.dev/ouster-detect/software_access/software_access.html)
- [Lidar Integration](https://static.ouster.dev/ouster-detect/lidar_integration.html)
- [Connecting to Output](https://static.ouster.dev/ouster-detect/connecting_to_output/connecting-to-output.html)
- [Code Sample Guide – TCP Output](https://static.ouster.dev/ouster-detect/appendix/appendix.html)

---

© 2025 Ouster, Inc. All rights reserved.